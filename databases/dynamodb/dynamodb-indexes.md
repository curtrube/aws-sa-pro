# DynamoDB Indexes

- Query is the most efficient operation in DynamoDB
- Query can only work on 1 PK value at a time
- ...and optionally a single, or range of SK values
- Indexes are `alternative views` on table data
- Different `SK (LSI)` or Different `PK and SK (GSI)`
- `Some` or `all attributes` (projection)

## Local Secondary Index (LSI)

- LSI is an alternative view for a table
- `MUST` be created with a table
- 5 LSI's per base table
- `Alternative SK` on the table
- `Shares` the `RCU` and `ECU` with the `table`
- Attributes - ALL, KEYS_ONLY & INCLUDE

## Global Secondary Index (GSI)

- Can be created `at any time`
- Default limit of `20 per base table`
- alternative `PK` and `SK`
- GSI's have their `own RCU` and `WCU` allocation
- Attributes - ALL, KEYS_ONLY & INCLUDE

## Considerations

- Careful with projection (KEYS_ONLY, INCLUDE, ALL)
- Queries on attributes NOT projected are expensive
- Use `GSI's as default`, LSI only when `strong consistency` is requried
- Use indexes for `alternative access patterns`