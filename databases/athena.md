# Athena

- `Serverless` Interactive Querying Service
- Ad-hoc queries on data - pay only `data consumed`
- `Schema-on-read` - table-like translation
- Origianl data `never changed - remains on S3`
- Schema translates data => relational-like when read
- Supports standard formats of structured, semi-structured and unstructured data.

## Process

- Source data stored in S3
- `"Tables"` are defined in advance in a data catalog and data is `projected through` when `read`. It allows `SQL-like` queries on data without `transforming` source data.

## Test Considerations

- Queries where `loading`/`transformation` `isn't desired`
- `Occasional` / `Ad-hoc` queries on data in S3
- `Serverless querying` scenarious - cost conscious
- Querying `AWS logs` - VPC Flow logs, CloudTrail, ELB logs, cost reports etc...
- AWS `Glue Data Catalog` & `Web Server Logs`
- w/ `Athea Federated Query`... `other data sources`