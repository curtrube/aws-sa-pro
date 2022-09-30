# S3 Presigned URLS

## Exam Power Up!

- You can create a URL for an objet you have `no access to`
- When using the URL, the permissions match the `identity which generated it`
- Access denied could mean the generating ID `never had access` or `doesn't have access now`
- `Don't generate with a role`... URL stops working when temporary credentials expire
