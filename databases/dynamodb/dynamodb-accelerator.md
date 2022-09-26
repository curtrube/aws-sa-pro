# DynamoDB Accelerator (DAX)

- in-memory cache specifically for DynamoDB
- runs within a VPC & AZ's
- primary read/write DAX node
- replicates to secondary read-replicas

## Considerations

- `Primary` NODE (`Writes`) and `Replicas` (`Read`)
- Nodes are `HA`.. Primary failure = election
- In-Memory cache - Scaling.. `Much faster reads, reduced costs`
- Scale `UP` and Scale `OUT` (`Bigger` and `More`)
- Supports `write-through`
- DAX deployed `within a VPC`