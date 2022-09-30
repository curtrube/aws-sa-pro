# Amazon Macie

- Data `Security` and Data `Privacy` Service
- `Discover`, `Monitor` and `Protect` Data stored in `S3` Buckets
- `Automated` discovery of data i.e. `PII`, `PHI`, `Finance`
- `Managed` Data Identifiers - `Built-in` - ML/Patterns
- `Custom` Data Identifiers - `Proprietary` - Regex Based
- Integrates with Security Hub & `finding events` to EventBridge
- Centrally manage.. either via `AWS Org` or one Macie Account `Inviting`

## Data Identifiers

### 1. Managed

- `Managed` data identifiers - maintained by AWS
- .. growing list of common sensitive data types
- Credentials, finance, health, personal identifiers

### 2. Custom

- `Custom` data identifiers - created by `you`
- `Regex` - defines a `pattern` to match in data
- `Keywords` - optional sequence that need to be in proximity to regex match
- `Maximum Match Distance` - how close keywords are to regex pattern
- `Ignore Words` - if regex match contains ignore words, it's ignored

## Finding Types

- `Policy` Findings or `Sesitive data` findings
- Policy findings when policies or settings for an S3 bucket are changed that reduces the security or privacy of the bucket or bucket's objects
- Sesitive Data is discovered in S3 objects