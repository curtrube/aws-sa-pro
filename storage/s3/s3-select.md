# S3 Select & Glacier Select

- S3 can store HUGE objects (up to `5TB`)
- You often want to retrieve the `entire object`
- Retrieving a 5TB object, `takes time`, `uses 5TB`
- Filtering at the client side `doesn't reduce this`
- S3/Glacier Select let you use a `SQL-like statement`
- ... to select part of the object, `pre-filtered by S3`
- `CSV`, `JSON`, `Parquet`, `BZIP2` compression for `CSV` and `JSON`