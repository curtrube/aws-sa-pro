# DynamoDB Global Tables

- Global tables provides `multi-master cross-region` replication
- All tables can be used for `Read` and `Write` operations
- Tables are created in multiple regions and added to the same global table (becoming replica tables)
- `Last writer wins` is used for conflict resolution
- `Reads` and `Writes` can occur to any region
- Generally `sub-second` replication between regions
- `Global eventual consistency` same-region `eventual` or `strongly` consistent
- Strongly consistent ready `ONLY` in the same region as writes
- Provides `Global HA` and `Global DR/BC`