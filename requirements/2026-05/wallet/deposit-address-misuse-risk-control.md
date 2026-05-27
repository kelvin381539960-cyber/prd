# Deposit Address Misuse Risk Control PRD

## 业务流程图

```mermaid
sequenceDiagram
    autonumber
    participant U as 用户
    participant A as AIX App
    participant D as DTC
    participant R as 充值记录

    U->>A: 进入充值并选择币种和网络
    A->>D: 获取收款页信息
    D-->>A: 返回收款地址、最低充值金额、网络信息
    A->>U: 展示收款页

    U->>A: 选择转账来源

    alt 来源是 Binance
        U->>D: 从 Binance 发起充值
        D->>R: 充值成功
        R-->>U: AIX 展示到账成功

    else 来源是我的钱包 App
        A->>D: 查询已添加的钱包地址列表
        D-->>A: 返回白名单钱包地址列表

        alt 存在当前币种和网络可用的钱包地址
            A->>U: 用户选择本次使用的钱包地址
            U->>D: 从所选钱包地址发起充值
            D->>R: 充值成功
            R-->>U: AIX 展示到账成功

        else 不存在可用钱包地址
            U->>A: 提交新钱包地址和地址名称

            A->>D: 校验该钱包地址是否支持当前币种和网络
            Note over A,D: 包含：查询地址支持网络 + 查询网络支持币种

            alt 不支持当前币种或网络
                A->>U: 提示该钱包地址不可用于本次充值
            else 支持当前币种和网络
                A->>D: 添加白名单钱包地址
                D-->>A: 返回白名单地址记录

                A->>D: 启用白名单钱包地址
                D-->>A: 返回启用结果

                alt 启用成功
                    A->>U: 钱包地址可用于本次充值
                    U->>D: 从新增钱包地址发起充值
                    D->>R: 充值成功
                    R-->>U: AIX 展示到账成功
                else 启用失败
                    A->>U: 提示钱包地址暂不可用
                end
            end
        end

    else 来源是其他交易所
        A->>U: 提示当前不支持其他交易所充值
    end
```

## DTC 接口说明

| 业务动作 | DTC 接口 |
|---|---|
| 查询已添加钱包地址 | `POST /openapi/v1/recipient/wallet-address/search` |
| 校验钱包地址支持网络 | `GET /openapi/v1/recipient/wallet-address/network/{address}` |
| 校验网络支持币种 | `GET /openapi/v1/recipient/wallet-address/currency/{mainNet}` |
| 添加白名单钱包地址 | `POST /openapi/v1/recipient/wallet-address/add-client-own` |
| 启用白名单钱包地址 | `POST /openapi/v1/recipient/wallet-address/set-enabled` |

## 当前定版口径

用户进入充值后，先选择币种和网络并进入收款页。用户在使用收款地址前，需要选择本次转账来源。

如果来源为 Binance，则沿用现有支持流程。

如果来源为我的钱包 App，AIX 先查询当前币种和网络下是否存在可用白名单钱包地址；存在则用户选择后继续，不存在则引导新增白名单钱包。

如果来源为其他交易所，则提示当前不支持，避免用户继续使用地址发起不支持来源的充值。

新增钱包地址时，AIX 需通过 DTC 完成支持性校验、添加白名单地址、启用白名单地址；启用成功后，该钱包地址可用于当前充值。
