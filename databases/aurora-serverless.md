# AWS Aurora Serverless

- Scalable - `ACU` - Aurora Capacity Units
- Aurora Serverless cluster has a `MIN` & `MAX` `ACU`
- Cluster adjusts based on load
- Can go to `0` and be `paused`
- Consumption billing per-second basis
- Same resilience as Aurora (6 copies across AZs)

## Use Cases

- `Infrequently` used applications
- `New` applications
- `Variable` workloads
- `Unpredictable` workloads
- `Development` and `test` databases
- `Multi-tenant` applications