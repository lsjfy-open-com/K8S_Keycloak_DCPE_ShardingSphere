# D. FAQ

## D.1 部署相关问题

### Q1: Keycloak集群如何配置高可用？
**A**: 使用JDBC_PING发现协议，配置3个以上Master节点，启用Redis缓存。

### Q2: ShardingSphere Proxy如何连接多个数据库？
**A**: 在`server.yaml`中配置多个数据源，使用分片规则路由。

### Q3: Milvus如何实现数据持久化？
**A**: 配置对象存储（MinIO/S3）作为存储后端，启用数据快照。

## D.2 运维相关问题

### Q4: 如何监控Keycloak性能？
**A**: 启用Keycloak metrics端点，集成Prometheus采集指标。

### Q5: 数据库连接池如何调优？
**A**: 根据QPS调整`maximumPoolSize`，监控连接等待时间。

### Q6: 证书过期如何处理？
**A**: 使用证书管理UI上传新证书，系统自动更新并重启服务。

## D3. 安全相关问题

### Q7: 如何保护数据库凭证？
**A**: 使用HashiCorp Vault存储，动态生成数据库凭证。

### Q8: 如何实现细粒度访问控制？
**A**: 结合ShardingSphere数据脱敏和OPA策略引擎。

### Q9: 审计日志如何配置？
**A**: 启用Keycloak审计日志，配置ELK收集和分析。

## 相关文档

- [技术选型参考](./A-技术选型参考.md)
- [配置模板](./B-配置模板.md)
- [术语表](./C-术语表.md)
