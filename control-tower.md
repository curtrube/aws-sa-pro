# AWS Control Tower

- `Quick` and `Easy` setup of `multi-account` environment
- `Orchestrates` other AWS services to provide this functionality
- Organizations, IAM Identity Center, CloudFormation, Conifg and more..
- `Landing Zone` - `multi-acccount` environment
- SSO/ID Federation, Centralized Logging and Auditing
- `Guard Rails` - `Detect/Mandate` rules/standards across all accounts
- `Account Factory` - Automation and Standardises new account creation
- `Dashboard` - single page oversight of the entire environment

## Landing Zone

- Designed to implement `Well Architected` mutli-account environment - Hom Region
- ...built with AWS `Organizations`, AWS `Config`, `CloudFormation`
- `Security OU` - Log Archive & Audit Accounts (`CloudTrail` & `Config Logs`)
- `Sandbox OU` - Test/less rigid security
- You can create other OU's and Account
- `IAM Identity Center` (AWS SSO) - `SSO`, `multiple-accounts`, `ID Federation`
- Monitoring and Notifications - CloudWatch and SNS
- `End User` account `provisioning` via `Service Catalog`

## Guard Rails

- Guardrails are rules - multi-account governance
- Mandatory, Stronly Recommended or Elective
- `Preventive` - Stop you doing things (AWS ORG SCP)
- ...enforced or not enabled
- i.e. allow or deny regions or disallow bucket policy changes
- `Detective` - compliance checks (AWS Config Rules)
- ...clear, in violation or not enabled
- .. detect CloudTrail enabled or EC2 Public IP

## Account Factory

- `Automated` Account `provisioning`
- ... cloud `admins` or `end users` (with appropriate permissions)
- `Guardrails` - `automatically` added
- Account `admin` given to a `named user` (IAM Identity Center)
- Account and network `standard configuration`
- Accounts can be `closed` or `repurposed`
- Can be fully `integrated` with a business `SDLC`