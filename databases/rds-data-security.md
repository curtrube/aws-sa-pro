# RDS Data Security

- `SSL/TLS` (`in transit`) in avaiable for RDS, can be `mandatory`
- RDS supports `EBS volume` encryption - `KMS`
- Handled by `HOST`/`EBS`
- AWS or Customer Managed CMK generates `data keys`
- `Data keys` used for `encryption` `operations`
- `Storage`, `Logs`, `Snapshots` & `replicas` are encrypted
- ....`encryption can't be removed`

### Encryption & TDE

- RDS `MS SQL` and RDS `Oracle` Support TDE
- `Transparent Data Encryption`
- Encryption handled `within the DB engine`
- RDS `Oracle` supports integration with `CloudHSM`
- Much stronger key controls (even from AWS)

#### TDE is `native DB encryption`. Data is encrypted before leaving the instance.
- With RDS Oracle - keys can be provided via CloudHSM
- Removes AWS from the chain of trust

#### KMS provides AWS or Customer Managed `CMK`'s which are used to generate Data Encryption Keys (`DEK`'s) for RDS
- DEK's loaded onto hosts as required (used by the host to perform encryption and decryption)

## IAM Authentication

- RDS local DB account configured to use AWS Authentication Token
- RDS instance role maps to a IAM policy 
- IAM policy used to `generate-db-auth-token` with a token with a 15 minute validity which can be used in the place of a DB User password