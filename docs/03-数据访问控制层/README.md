# 数据访问控制层

## 模块概述

本模块负责实现基于Apache ShardingSphere和OPA的数据访问控制方案，在不修改客户表结构的情况下实现表级和列级的访问控制。

## 目录结构

```
03-数据访问控制层/
├── README.md                    # 本文档
├── 3.1-访问控制引擎.md          # ShardingSphere + OPA集成
├── 3.2-ODBC数据访问层.md        # ODBC组件开发
├── 部署配置/
│   ├── sharding-proxy.yaml
│   ├── opa-config.yaml
│   └── encrypt-rules.yaml
└── 代码示例/
    ├── SecureQueryBuilder.java
    └── OpaPolicyEngine.java
```

## 核心功能

### 3.1 访问控制引擎
- Apache ShardingSphere Proxy部署与配置
- OPA（Open Policy Agent）策略引擎集成
- 数据脱敏规则配置
- 访问策略定义与管理
- 统一访问控制API设计

### 3.2 ODBC数据访问层
- 通用ODBC数据访问组件开发
- ShardingSphere JDBC集成
- 数据库连接池管理
- 异常处理与日志记录
- 查询性能优化与批处理

## 技术栈

- **数据库中间件**: Apache ShardingSphere 5.3.x
- **策略引擎**: Open Policy Agent 0.55.x
- **连接池**: HikariCP 4.x
- **ODBC**: unixODBC / iODBC

## 交付物清单

1. ShardingSphere部署配置
2. OPA策略配置
3. 数据脱敏规则文档
4. API接口文档
5. 策略管理平台
6. ODBC组件源代码
7. 连接池配置文档

## 8人分工

| 人员 | 职责 | 工作量占比 |
|-----|------|-----------|
| 人员3 | 数据安全工程师 | 20% |
| 人员4 | 数据访问工程师 | 15% |

## 相关文档

- [主项目文档](../项目工作分解结构.md)
- [技术方案](../07-技术方案/README.md)
- [任务拆分](../08-任务拆分/README.md)

## 联系方式

模块负责人：数据安全工程师（人员3）
