# K8s多租户部署方案 - Keycloak + DCPE + ShardingSphere

## 项目概述

将内部K8s多Pod应用部署到客户环境的完整技术方案，涉及：
- **身份认证**：基于Keycloak的多租户OAuth2/OIDC认证
- **数据访问控制**：Apache ShardingSphere + OPA实现表级和列级访问控制
- **向量数据库**：Milvus + DCPE加密算法安全增强
- **安全存储**：K8s Secret + HashiCorp Vault密钥管理

## 技术栈

| 组件 | 推荐方案 | 版本 |
|-----|---------|------|
| 身份认证 | Keycloak | 22.x/23.x |
| 数据访问控制 | Apache ShardingSphere + OPA | 5.3.x / 0.55.x |
| 向量数据库 | Milvus | 2.3.x |
| API网关 | Kong | 3.x |
| 密钥管理 | HashiCorp Vault | 1.13.x |
| 容器编排 | Kubernetes | 1.28.x |

## 目录结构

```
K8S_Keycloak_DCPE_ShardingSphere/
├── 01-身份认证与多租户/          # Keycloak多租户架构设计
├── 02-K8s安全与Secret管理/       # K8s Secret安全方案
├── 03-数据访问控制层/            # ShardingSphere + OPA
├── 04-Milvus向量数据库集成/      # DCPE加密向量数据库
├── 05-应用服务与网关/            # API网关与服务网格
├── 06-部署与运维/                # CI/CD、监控、日志
├── 07-技术方案/                  # 详细技术方案文档
├── 08-任务拆分/                  # 8人分工任务拆分
├── 99-附录/                      # 参考资料、配置模板
├── 项目工作分解结构.md            # 主文档
└── README.md                     # 本文档
```

## 核心功能模块

### 1. 身份认证与多租户
- Keycloak多租户架构设计
- AD/LDAP Federation集成
- 租户识别与隔离
- 统一身份映射

### 2. K8s安全与Secret管理
- Secret静态加密
- 密钥自动轮换
- RBAC访问控制
- HashiCorp Vault集成

### 3. 数据访问控制层
- Apache ShardingSphere数据脱敏
- OPA策略引擎集成
- 表级和列级访问控制
- ODBC数据访问组件

### 4. Milvus向量数据库集成
- DCPE加密算法集成
- 向量访问控制
- 权限级别管理
- 加密向量检索

## 8人分工

| 人员 | 角色 | 职责领域 | 工作量占比 |
|-----|------|---------|-----------|
| 人员1 | 身份认证架构师 | 身份认证与多租户 | 20% |
| 人员2 | 安全工程师 | K8s安全 | 15% |
| 人员3 | 数据安全工程师 | 数据访问控制 | 20% |
| 人员4 | 数据访问工程师 | 数据访问层 | 15% |
| 人员5 | 向量数据库工程师 | 向量数据库 | 10% |
| 人员6 | 网关架构师 | 网关与服务 | 10% |
| 人员7 | 运维工程师 | 部署运维 | 5% |
| 人员8 | 全栈开发工程师 | 集成开发 | 5% |

## 实施阶段

1. **阶段1**：基础架构搭建（2周）
2. **阶段2**：核心功能开发（4周）
3. **阶段3**：安全加固（2周）
4. **阶段4**：部署与运维（2周）

## 快速开始

### 环境要求
- Kubernetes 1.28+
- Helm 3.10+
- Docker 24.x+
- kubectl配置完成

### 部署步骤
```bash
# 1. 克隆项目
git clone https://github.com/lsjfy-open-com/K8S_Keycloak_DCPE_ShardingSphere.git
cd K8S_Keycloak_DCPE_ShardingSphere

# 2. 部署Keycloak
kubectl apply -f 01-身份认证与多租户/部署配置/

# 3. 部署ShardingSphere
kubectl apply -f 03-数据访问控制层/部署配置/

# 4. 部署Milvus
kubectl apply -f 04-Milvus向量数据库集成/部署配置/
```

## 文档导航

- [项目工作分解结构](项目工作分解结构.md)
- [技术方案](07-技术方案/README.md)
- [任务拆分](08-任务拆分/README.md)
- [附录](99-附录/README.md)

## 贡献者

项目团队：8人开发小组

## 许可证

MIT License

## 联系方式

GitHub: [lsjfy-open-com](https://github.com/lsjfy-open-com)

---

**最后更新**: 2026-02-01
**版本**: 2.0
