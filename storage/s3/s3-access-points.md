# S3 Access Points

- `Simplify managing` access to S3 Buckets/Objects
- Rather than 1 bucket w/ 1 `complex` Bucket Policy
- Create `many` access points
- each with `different policies`
- each with `different network access controls`
- Each access point has it's own endpoint address
- Created via Console or `aws s3control create-access-point` --name `foo` --account-id `bar` --bucket `foobar`