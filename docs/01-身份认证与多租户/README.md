# 身份认证与多租户架构

## 模块概述

本模块负责实现基于Keycloak的多租户身份认证架构，对接客户AD（Active Directory），实现统一的身份认证和权限管理。

## 目录结构

```
01-身份认证与多租户/
├── README.md                    # 本文档
├── 1.1-Keycloak多租户架构设计.md
├── 1.2-AD集成与身份映射.md
├── 架构设计文档.md
└── 部署配置/
    ├── keycloak-deployment.yaml
    ├── realm-configuration.md
    └── ad-federation-config.md
```

## 核心功能

### 1.1 Keycloak多租户架构设计
- Realm规划与租户隔离策略
- Client Scope实现租户数据隔离
- 基于Client的访问策略配置
- 租户识别机制（域名/邮箱后缀/请求头）

### 1.2 AD集成与身份映射
- LDAP/AD Federation配置
- 用户属性映射规则设计
- 租户识别逻辑实现
- AD组到应用角色的映射
- 跨租户会话管理

## 技术栈

- **Keycloak**: 22.x/23.x
- **AD Federation**: LDAP/Active Directory
- **认证协议**: OAuth2/OIDC, SAML 2.0

## 交付物清单

1. 架构设计文档（PDF）
2. Keycloak集群部署方案
3. 多租户认证流程图
4. Realm规划文档
5. AD集成配置文档
6. 身份映射规则配置
7. 角色映射矩阵
8. 会话管理方案

## 8人分工

| 人员 | 职责 | 工作量占比 |
|-----|------|-----------|
| 人员1 | 身份认证架构师 | 20% |
| 人员2 | 安全工程师（AD集成） | 15% |

## 相关文档

- [主项目文档](../项目工作分解结构.md)
- [技术方案](../07-技术方案/README.md)
- [任务拆分](../08-任务拆分/README.md)

## 联系方式

模块负责人：身份认证架构师（人员1）
