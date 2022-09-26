# DynamoDB Time-to-Live (TTL)

- Timestamp for `automatic` `DELETE` of ITEMS
- Define when a item is no longer needed
- When TTL is enabled on a table a specific `attribute` is selected for TTL

## Process

- A per-partition process `periodically` `runs`, checking the `current` time (in seconds since epoch) to the value in the `TTL attribute`
- ITEMS where the TTL attribute is older than the current time are set to expired
- Another per-partition background process scans for expired items