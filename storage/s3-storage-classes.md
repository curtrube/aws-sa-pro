# S3 Storage Classes

## S3 Standard (Default Storage Class)

- Objects are replicated across `at least 3 AZs` in the AWS region
- 99.999999999% (`11 x 9's`) durability for 10,000,000 objects, 1 object loss per 10,000 years
- Replication over 3 AZ's & Content-MD5 checksums and Cyclic Redundancy Check (CRC's) are used to detect and fix any data corruption
- When objects are stored successfully a HTTP/1.1 200 OK response is provided by the S3 api endpoint
- You are billed a `GB/month` for data stored
- A `$ per GB charge for transfer out` (`in` is `free`)
- A `price per 1,000 requests`
- `No` specific `retrieval fee`, `no minimum duration`, `no minimum size`
- S3 Standard has a `milliseconds first byte latency` and objects can be made publicly available

## Standard-Infrequent Access (IA)

- Designed for infrequently accessed data
- Per GB retrieval fee, overall cost increases with frequent data access.
- Minimum duration charge of 30 days
- Minimum capacity charge of 128KB per object
- Should be used for long lived data that is important and irreplaceable but is infrequently accessed.

## One Zone - Infrequent Access

- cheaper than s3 standard or standard-IA
- retrieval fee
- minimum duration charge
- minimum capacity charge
- `data is only stored in one AZ`
- should be used for long lived, infrequently accessed data that is non-critical or easily replaced

## Intelligent-Tiering

### Intelligent-Tiering Five Storage Tiers

1. Frequent Access
1. Infrequent Access
1. Archive Instant Access
1. Archive Access
1. Deep Archive

- Intelligent-Tiering `monitors` and `automatically` moves any objects `not accessed for 30 days` to a `low cost infrequent access tier` and eventually to `archive instant access`, `archive access` or `deep archive tiers`
- As objects are `accessed`, they are `moved back to the frequent access` tier. There are `no retrieval fees` for access objects.
- Intelligent Tiering has a `monitoring and automation cost per 1,000 objects`. The frequent access tier costs the same as S3 Standard, the Infrequent the same as Standard-IA, Archive instant, Archive and Deep Archive are comparable to their S3 glacier equivalents.
- Designed for long-lived data with changing or unknown access patterns