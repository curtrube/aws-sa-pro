# S3 Replication

- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)

## Replication Configuration

- `All objects` or a `subset`
- `Storage Class` - default is to maintain
- `Ownership` - default is the source account
- Replication Time Control (`RTC`)
- `Versioning needs to be ENABLED` in both source and destination buckets
- `Not retroactive` existing objects will not be replicated prior to enabling replication
- `One-way replication` Source to Destination
- Unencrypted, SSE-S3, SSE-KMS (`with extra config`)
- Source bucket owner needs permissions to objects
- No `system events`, `Glacier`, or `Glacier Deep Archive`
- `NO DELETES` - by default S3 does not replicate delete markers

## Why use replication?

- SRR - Log Aggregation
- SRR - PROD and TEST sync
- SRR - Resilience with strict sovereignty
- CRR - Global Resilience Improvements
- CRR - Latency Reduction