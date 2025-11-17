S3 Basics (Simple Notes)

These are my beginner notes on Amazon S3, written to help me remember the core ideas and how the service works.

**What is S3?

Amazon S3 (Simple Storage Service) is AWS’s object storage service.
You store files as objects inside buckets.

** Key Terms

Bucket: A container for your files

Object: The actual file you upload

Region: Buckets live in a specific AWS region

Key: The name/path of the object inside the bucket

**Access & Permissions

S3 uses IAM policies and bucket policies to control:

Who can access the bucket

Who can upload or delete files

Whether the bucket is public or private

Default: All buckets are private.

** Common Actions

Create a bucket

Upload files

Download or view files

Make a file public (only when needed)

Enable versioning (to keep older versions of files)

Turn on encryption

Storage Classes (Basic Ones)

Standard: Default, frequent access

Standard-IA: Infrequent access

Glacier: Long-term archival

**Why S3 Is Useful

Stores files reliably

Scales automatically

Great for hosting static websites

Used in almost every cloud project

 **Status

These notes will expand as I learn more about S3.
