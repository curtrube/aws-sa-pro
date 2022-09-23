# Directory Service - AD Connector

- A `pair` of directory endpoints `running in AWS` (`ENI's in VPC`)
- Supports directory aware AWS products
- `Redirects requests` to `existing directory servers`
- `No directory data` stored in AWS... `all redirected`
- Use `existing on-premises AD` with `directory compatible AWS Services` without any identity data in AWS
- `Proof of concepts` where you need to use existing identities.
- Two sizes.. `small` and `large`.. no explicit user limits between the two
- size controls the amount of compute allocated
- Multiple AD Connectors can be used to spread load
- Requires `2 subnets` within a VPC.. `different AZ's`
- Connector requires 1 or more directory server(s) to be configured
- `REQUIRES` a `working network` connection (no caching or data saved in AWS)
- Network connectivity via `Direct Connect` or `VPN`