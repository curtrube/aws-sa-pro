# AWS S3 Glacier

## Instant

- like S3 Standard-IA... cheaper storage, more expensive retrieval, longer minimum
- still have instant access to data

## Flexible

- `data in a chilled state`
- same 3-AZ's avaiability
- same durability (11x 9's)
- about 1/6th cost of S3 standard
- treat as `cold` objects
- aren't immediately available
- any access of data requires a `retrieval process`
- 40KB minimum size
- 90 Day minimum duration
- 

### Glacier `Flexible` Retrieval Types

- `Expedited` (1-5 minutes)
- `Standard` (3-5 hours)
- `bulk` (5-12 hours)
- `Faster = More Expensive`
- `First byte latency = minutes or hours`

- Used for archives where frequent to data isn't necessary (maybe once a year)
- one of the cheapest forms of storage in S3, as long as you can tolerate the characteristics of the storage class.

## Deep Archive 

- much cheaper than flexible storage type
- `data in a frozen state`
- objects have 50KB minimum size
- 180 day minimum billable duration
- objects cannot be made publicly accessible
- jobs temporariliy restore data to s3 standard access
- used for data archival where access is rarely `IF` ever needed

### Glacier `Deep Archive` Retrieval Types
- Much longer than Glacier Flexible
- Standard (12 hours)
- Bulk (up to 48 hours)
- `First byte latency = hours or days`