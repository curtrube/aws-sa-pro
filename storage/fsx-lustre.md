# FSx for Lustre

- Managed `Lustre` - Designed for `HPC` - `Linux` Clients (POSIX)
- `Machine Learning`, `Big Data`, `Financial Modelling`
- `100's GB/s` throughput & `sub millisecond` latency
- Deployment types - `Persistent` or `Scratch`
- Scratch - Highly optimised for `Short term` no replication & fast
- Persistent - `longer term`, `HA` (in one AZ), `self-healing`
- Accessible over `VPN` or `Direct Connect`

- Metadata stored on Metadata Targets (`MST`)
- Objects are stored on object storage targets (`OSTs`) (`1.17TiB`)
- `Baseline` performance based on size
- Size - min `1.2TiB` then increments of `2.4TiB`
- For `Scratch` - Base 200MB/s per TiB of storage
- Persistent offers `50MB/s`, `100MB/s`, and `200MB/s` per TiB of storage
- Burst up to `1,300MB/s` per TiB (credit system)

- Scratch is designed for `pure performance`
- `Short term` or temp workloads
- `NO HA`.. `No replication`
- `Larger file systems` means more servers, more disks and `greater change of failure`
- Persistent has `replication` within `One AZ` only
- `Auto-heals` when hardware failure occurs
- You can `backup to S3` with `both`! (Manal or automatic 0-35 day retention)