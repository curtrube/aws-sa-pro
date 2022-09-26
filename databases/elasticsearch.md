# Elasticsearch (ES)

- Managed implementation of Elasticsearch
- ... open source search product
- `ELK` Stack .. `E`S, `K`ibana and `L`ogstash
- `It's not serverless`.. it runs in a VPC using compute
- Alternative to AWS services - `if you already use ES/ELK`
- Log analytics, monitoring, security analytics, full text search and indexing, clickstream analytics
- Doesn't have as tight of integration with other AWS services

## ELK Stack

- `Elasticsearch` - `Search` and `Indexing`
- ... in a VPC, uses compute
- `Kibana` - visualization / dashboards
- `Logstash` - similar to `CWLogs`, needs a `Logstash agent` installed on anything to 'ingest' the data
