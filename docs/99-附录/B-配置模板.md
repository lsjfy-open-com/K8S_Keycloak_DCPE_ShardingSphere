# B. 配置模板

## B.1 K8s Secret加密配置模板

```yaml
# encryption-config.yaml
apiVersion: apiserver.config.k8s.io/v1
kind: EncryptionConfiguration
resources:
  - resources:
    - secrets
    - configmaps
    providers:
    - aescbc:
        keys:
        - name: key1
          secret: <base64-encoded-key-32bytes>
    - identity: {}
```

## B.2 Keycloak Realm配置模板

```json
{
  "realm": "customer-realm",
  "enabled": true,
  "loginTheme": "base",
  "registrationAllowed": false,
  "loginWithEmailAllowed": true,
  "duplicateEmailsAllowed": false,
  "resetPasswordAllowed": false,
  "editUsernameAllowed": false,
  "bruteForceProtected": true
}
```

## B.3 ShardingSphere数据脱敏配置模板

```yaml
rules:
  - tables:
      customer_info:
        columns:
          phone:
            encryptorName: phone_encryptor
            type: AES
          salary:
            encryptorName: salary_encryptor
            type: AES
        queryWithCipherColumn: false
  encryptors:
    phone_encryptor:
      type: AES
      props:
        aes-key-value: your-aes-key
```

## B.4 OPA策略配置模板

```rego
package data_access

allow_column(table, column, role) {
    role == "admin"
    allow_table(table, role)
}

allow_table(table, role) {
    role == "admin"
}
```

## B.5 Kong网关配置模板

```yaml
apiVersion: configuration.konghq.com/v1
kind: KongPlugin
metadata:
  name: rate-limit
config:
  minute: 100
  hour: 1000
  policy: local
```

## 相关文档

- [技术选型参考](./A-技术选型参考.md)
- [术语表](./C-术语表.md)
