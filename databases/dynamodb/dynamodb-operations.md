# DynamoDB Operations, Consistency and Performance

## Reading and Writing

- `On-Demand` - unknown, unpredictable, low administration
- On-Demand - price `per million` R or W units
- Provisioned... RCU and WCU set on a per table basis
- Every operation consumes at least `1RCU/WCU`
- 1 RCU is `1 x 4KB` read operation per second
- 1 WCU is `1 x 1KB` write operation per second
- Every table has a RCU and WCU burst pool (`300 seconds`)

### Query

- most efficient operation in DynamoDB
- Query accepts a single PK value and *optionally* a SK or range.
- Capacity consumed is the size of `all returned items`
- Further filtering discards data - capacity is still consumed.
- `Can ONLY query on PK or PK and SK`

### Scan

- least efficient operation in DynamoDB
- Scan moves through the table consuming the capacity `of every ITEM`.
- You have complete control on what data is selected
- `Any attributes` can be used and `any filters` applied but SCAN consumes capacity for `EVERY Item` scanned.

## Consistency Model

### Eventually Consistent Reads

- (default)
- response might not reflect the most recently completed operation
- the response might include some stale data
- if you repeat the request after a short time, the reponse should return the latest data

### Strongly Consistent Reads

- response returns the most up-to-date data

    #### Disadvantages

        - use more throughput capacity
        - higher latency
        - not supported on global secondary indexes
        - higher dependence on good network connectivity