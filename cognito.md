# Cognito

- `Authentication`, `authorication` and `user management` for web/mobile applications.

## User Pools

- sign-in and get a JSON web token (JWT)
- Colleciton of Identities of users used for sign-up and sign-in both for internal users and social sign-in.
- User directory management and profiles
- sign-up & sign-in (customisable web UI)
- MFA and other security features.

## Identity Pools

- Allow you to access `Temporary AWS Credentials`
- Unauthenticated Identiies - Guest Users (store data from a mobile app without user sign-up)
- `Federated Identities` - Exchanges Google, Facebook, Twitter, SAML2.0, & User Pool credentials for short term AWS credentials to acess AWS resources
- `SWAP` external identities for temporary AWS credentials `(called Federation)`