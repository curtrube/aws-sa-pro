# AWS Quantum Ledger Database (QLDB)

- `Immutable append-only` `ledger` based database
- `Cryptographically verifiable` transaction log
- `Transparent` - full history is always accessible
- `Serverless` - Provides Ledger and Tables - no server
- `3-AZ resillience` & replication `within each AZ`
- Can `stream` data to `Amazon Kinesis`
- `Document` DB model
- `ACID` - Tansfer A -> B... either `both` work or `none` work

# Use Cases

- `Finance` - account balances & transactions
- `Medical` - full history of data changed
- `Logistics` - track movement of objects
- `Legal` - track usage and change of data (custody)