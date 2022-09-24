# AWS RDS (Relational Database Service)

- Database-as-a-service (`DBaaS`)
- ...`DatabaseServer`-as-a-service (more accurate description)
- `Managed Database` Instance (1+ Databases)
- Multiple engines `MySql`, `MariaDB`, `PostgreSQL`, `Oracle`, Microsoft `SQL Server`.
- ... `Amazon Aurora`

## RDS Instance

- Access the RDS instance via a `CNAME` record
- The `CNAME` always points at the `primary` RDS instance

### Multi-AZ Instance

- Create a `primary DB` instance and a `standby DB` instance in a `different AZ`
- `Synchronous replication` between the primary and stanby db instance (`near real time replication`)
- The standby instance does not improve performance, only avaiable in the event the primary goes down.

## Important Points

- No `Free-tier` for Multi-AZ RDS deployment
- Standby DB instance can't be directly used
- `60-120` seconds to failover
- `Same region only` (other AZ's in the VPC)
- Backups taken `from Standby` (removes performance impact)
- AZ Outage, Primary Failure, Manual failover, Instance type change and software patching
- Only benefits of Multi-AZ is availability not performance. Minimize distruptions around software patching and backups.

## Backup and Restore

### RPO vs. RTO

### Recovery Point Objective (RPO)

- Time between last backup and the db failure
- Amount of maximum data loss
- Influences technical solution and cost
- Generally lower values cost more

### Recovery Time Objective (RTO)

- Time between a db failure and full recovery
- Influenced by process, staff, tech and documentation
- Generally lower values cost more

### Backups

- Automatic Backups
- Manual Snapshots

### Restores

- Creates a `NEW RDS Instance` - new address
- Snapshots = `single point in time`, creation time
- Automated = any 5 minute point in time
- Backup is restored and transaction logs are 'replayed' to bring the DB to desired point in time
- Restores `aren't fast` - Think about `RTO`