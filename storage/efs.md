# Elastic File System (EFS)

- `EFS` is an implementation of `NFSv4`
- EFS `Filesystems` can be `mounted in Linux`
- `Shared` between many EC2 Instances
- Private service, via `mount targets` inside a VPC
- Can be accessed from on-premises - `VPN` or `DX`

## Architecture 

- `Linux Only`
- `General Purpose` and Max I/O performance modes
- General Purpose = default for 99.9% of uses
- `Bursting` and `Provisioned` throughput modes
- `Standard` and `Infrequent` Access (IA) classes
- Lifecycle Policies can be used with classes
- Encryption at rest using KMS