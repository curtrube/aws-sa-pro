# S3 Object Lock

- Object Lock enabled on `new` buckets* (Support req for existing bucket)
- Write-One-Read-Many (`WORM`) - `No Delete`, `No Overwrite`
- Requires `versioning` - `individual versions` are locked
- Two types of `object retention`:
    1. `Retention Period`
    1. `Legal Hold`
- Objects can use `Both`, `One`, or `the other`, or `none`
- A Bucket can have default `Object Lock` settings

## Retention Period

- Specify `DAYS` & `YEARS` - A Retention Period for the object

### `COMPLIANCE` Mode

- `Can't` be `adjusted`, `deleted`, `overwritten` by any user, including the account root user
- `Until the retention expires`

### `GOVERNANCE` Mode

- Objects can't be changed during the retention period
- special `permissions` can be granted allowing lock settings to be adjusted
    - `s3:BypassGovernanceRetention` policy

## Legal Hold

- Set on an object version - `ON` or `OFF`
- No retention
- `NO Deletes` or `Changes` until legal hold removed
- `s3:PutObjectLegalHold` is required to add or remove
- Prevent accidental deletion of critical object versions