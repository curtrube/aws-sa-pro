# DynamoDB Streams & Triggers

## Stream

- Time ordered list of `ITEM CHANGES` in a table
- `24-Hour` rolling window
- Enabled on a `per table` basis
- Records `INSERTS`, `UPDATES`, `DELETES`
- Different `view types` influence what is in the stream

### 4 view types

1. KEYS_ONLY
1. NEW_IMAGE
1. OLD_IMAGE
1. NEW_AND_OLD_IMAGES

## Triggers

- Action takes place when data changes
- ITEM `changes` generate an `event`
- That event `contains the data` which changed
- A `action is taken` using that data
- AWS = `Streams + Lambda`

### Use Cases
- `Reporting` & `Analytics` 
- `Aggregation`, `Messaging`, `Notifications`