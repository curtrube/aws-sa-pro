# AWS DynamoDB

- `NoSQL` managed Database-as-a-servide (DBaaS)
- `Key`/`Value` & `Document`
- `Public` Service
- `No self-managed servers` or infrastructure
- `Manual` / `Automatic` provisioned performance IN/OUT or `On-Demand`
- Highly Resilient ...across `AZ's` and optionally `global`
- `Really fast`... `single digit milliseconds` (SSD based)
- Backups, point-in-time recovery, encryption at rest
- Event-Driven integration... do things when data changes

## Tables

- A `Table` is a grouping of `ITEMS` with the same `PRIMARY KEY`
- `Simple (Partition)` or `Composite (Partition & Sort)` `Primary Key`
- Each item `MUST` have a unique value for PK and SK. Can have none, all, mixture or different attributes
- Item MAX `400KB`

## Capacity

- `Capacity` relates to speed in DynamoDB

    ### `On-Demand`

    - No explicit values configured
    - Scales automatically

    ### `Provisioned`

    - Write Capacity Units (WCU)

        - 1 WCU = 1KB per second

    - Read Capacity Units (RCU)

        - 1 RCU = 4KB per second

## Backups

- `On-Demand` 
    - Full copy of Table
    - Retained until Removed
    - Restore:
        - Same or Cross-Region
        - with or without Indexes
        - Adjust encryption settings

- `Point-In-Time-Recovery`
    - Not Enabled by Default
    - Continuous record of changes allow `replay to any point` in the window
    - 35 day recovery window
    - 1 second granularity

## Considerations

- NoSQL... `preference` DynamoDB in the exam
- Relational Data... generally `NOT` DynamoDB
- Key/Value... `preference` DynamoDB in the exam
- Access via console, CLI, API.. '`No SQL`'
- Billed based `RCU`, `WCU`, `Storage` and `features`