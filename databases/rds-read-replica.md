# AWS RDS Read-Replica

- Kept in sync using `Asynchronous Replication` (written on primary first and then replicated to the read-replica)
- Can be created in same region and primary or different region
- Can't be used for `writes`, only `reads`.


### Performance Improvements

- `5x` direct read-replicas per DB instance
- Each providing an `additional instance of read performance`
- Read-Replicas can have read-replicas - `but lag starts to be a problem`.
- `Global` performance improvements

### Availability Improvements

- Snapshots & Backups Improve RPO
- RTO's are a problem
- RR's offer `near 0 RPO`
- RR's can be `promoted quickly` - `low RTO`
- `Failure only` - watch for data corruption
- `Read only` - `until promoted`
- Global availability improvements.. global resilience