# C. 术语表

## C.1 身份认证术语

| 术语 | 英文 | 解释 |
|-----|------|------|
| OAuth2 | OAuth 2.0 | 开放授权协议，用于授权第三方应用访问资源 |
| OIDC | OpenID Connect | 基于OAuth2的身份认证协议 |
| SAML | Security Assertion Markup Language | 安全断言标记语言，用于单点登录 |
| JWT | JSON Web Token | JSON格式的令牌，用于安全传输信息 |
| Realm | Realm | Keycloak中的安全域，用于隔离用户和配置 |
| Client | Client | Keycloak中代表应用程序的实体 |
| Client Scope | Client Scope | Keycloak中用于定义令牌属性的作用域 |

## C.2 数据安全术语

| 术语 | 英文 | 解释 |
|-----|------|------|
| DCPE | Data Classification and Privacy Encryption | 数据分类与隐私加密算法 |
| RLS | Row-Level Security | 行级安全策略 |
| CLS | Column-Level Security | 列级安全策略 |
| DLP | Data Loss Prevention | 数据丢失防护 |
| PII | Personally Identifiable Information | 个人身份信息 |

## C.3 K8s术语

| 术语 | 英文 | 解释 |
|-----|------|------|
| Secret | Secret | K8s中用于存储敏感信息的资源 |
| ConfigMap | ConfigMap | K8s中用于存储非敏感配置的资源 |
| ServiceAccount | ServiceAccount | K8s中用于Pod身份认证的账户 |
| RBAC | Role-Based Access Control | 基于角色的访问控制 |
| mTLS | Mutual TLS | 双向TLS认证 |

## C.4 数据库术语

| 术语 | 英文 | 解释 |
|-----|------|------|
| ODBC | Open Database Connectivity | 开放数据库连接标准 |
| JDBC | Java Database Connectivity | Java数据库连接标准 |
| Connection Pool | Connection Pool | 数据库连接池，用于管理数据库连接 |
| Sharding | Sharding | 数据库分片，将数据分散存储 |

## C.5 向量数据库术语

| 术语 | 英文 | 解释 |
|-----|------|------|
| Vector | Vector | 向量，用于表示数据的数学形式 |
| Embedding | Embedding | 嵌入，将数据转换为向量表示 |
| Index | Index | 索引，用于加速向量检索 |
| ANN | Approximate Nearest Neighbor | 近似最近邻搜索 |

## 相关文档

- [技术选型参考](./A-技术选型参考.md)
- [配置模板](./B-配置模板.md)
