# Amazon Workspaces

- `Desktop-as-a-Service (DAAS)` - Home/Remote working office
- Similar to `Citrix/Remote Desktop` - Except hosted by AWS
- Consistent desktop from anywhere - apps and state
- `Windows` and `Linux` desktops - various sizes/configurations
- With or without AWS provided app & custom images
- `Monthly` or `Hourly` pricing (+base infrastructure cost)
- Uses `Directory Service` (`Simple`, `AD`, `AD Connector`) for authentication and user management.
- Workspace uses an `ENI` in a VPC... `uses VPC networking`
- Windows access `FSx` and `EC2` windows resources
- or on-premises resources over `VPN` or `Direct Connect`
- At-rest encryption (`EBS` + `KMS`)