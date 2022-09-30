# S3 Encryption

- Buckets aren't encrypted... `objects are`

## S3 Supports

- `Client`-Side Encryption (You control the end-to-end process)
- `Server`-Side Encryption (Allow S3 to handle part of the encryption)

### Client-Side Encryption

- You manage the Keys
- You manage the Encryption Processing

### Server-Side Encryption with Customer-Provided Keys (`SSE-C`)

- You manage the keys
- AWS S3 manages Encyrption/Decryption processing

### Server-Side Encryption with Amazon S3-Managed Keys (`SSE-S3`)

- AWS S3 Manages the `Root` Key used to encrypt the individual object encryption keys
- AWS S3 manages the Encryption/Decryption process
- No admin overhead
- User(s) have no control over the root key used for encryption

### Server-Side Encryption with KMS KEYS Stored in AWS Key Management Service (`SSE-KMS`)

- AWS Manages the Keys using S3 & Key Management Service (KMS)
- Requires KMS permissions to decrypt the KMS key
- Key rotation control & Role separation

## Default Bucket Encryption

- `Put:Object` x-amz-server-side-encryption - header
- If you don't specify this header, than objects won't be encrypted
- If you do specify this header;
    - AES256 = SSE-S3
    - aws:kms = SSE-KMS
    - default = Disabled