# S3 Encryption
## SSE-S3
* Server side ecnryption using AES 256
* Enabled by default for new objects and buckets
* Must set header "x-amz-server-side-encryption":"AES256"
* Enabled by default for new buckets and objects 
## SSE-KMS
* Server side ecnryption usingAWS KMS
* User controlled and can be audited using CloudTrail
* Must set header "x-amz-server-side-encryption":"aws:kms"
* Decryption and encryption done with KMS
* API calls to KMS will be limited per region
## SSE-C
* Server side ecnryption
* Key managed outside by user 
* HTTPS must be used and passed in HTTP header
* Keys not stored in S3
* Can only be done via the CLI, not the 
## SSE-Client side encryption
* Client side ecnryption and decryption
* Data encrypted before sending to S3
* Client manages the cycle completely
## Encryption in transit
* Force HTTPS by using "aws:SecureTransport":"false"
