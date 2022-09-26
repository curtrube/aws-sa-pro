# AWS Aurora

- Aurora architecture is `very` different from RDS
- Uses a `"Cluster"`
- A single `primary` instance + 0 or more `replicas`
- replicas can be used for reads
- No local storage - uses cluster volume
- Faster provisioning & imporoved availability & performance


## Storage Architecture

- All SSD based - `high IOPS, low latency`
- Storage is billed based on `what's used`
- `High water mark` - billed for the most used
- Storage which is freed up can be re-used
- Replicas can be added and removed wihtout requiring storage provisioning

## Cost

- No free-tier option
- Aurora doesn't support Micro Instances
- Beyond RDS singleAZ (micro) Aurora offers better value
- Compute - hourly charge, per second, 10 minute minimum
- Storage - GB-Month consumed, IO cost per request
- 100% DB Size in backups are included

## Restore, Clone & Backtrack

- Backups in Aurora work in the same way as RDS
- Restores create a `new cluster`
- Backtrack can be used which allow `in-place rewinds` to a previous point in time
- Fast clones make a new database MUCH faster than copying all the data - `copy-on-write`

## Multi-Master 

- Default Aurora mode in `Single Master`
- `One R/W` and `0+ Read Only` Replicas
- Cluster endpoint is used to write, read endpoint is used for load balanced reads
- Failover takes time - replica promoted to R/W
- In Multi-Master mode `all instances are R/W`
- 

## Single Master 