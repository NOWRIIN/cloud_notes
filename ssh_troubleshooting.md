SSH Troubleshooting Notes

These are my personal notes for fixing common SSH connection issues when connecting to an EC2 instance in AWS.
 1. Permission denied (publickey)

This usually means:

Wrong key pair

Wrong username

Wrong region

Key belongs to an old/terminated instance

✔️ Fixes

Make sure you are using the correct key from the EC2 launch

Check the EC2 instance username

Amazon Linux: ec2-user

Ubuntu: ubuntu

Make sure your instance is in the same region where your key pair exists

 2. Key file permissions too open

Error:

UNPROTECTED PRIVATE KEY FILE!


Fix:

chmod 400 mykey.pem

3. Security group is blocking SSH

Check the security group for:

Inbound rule: SSH (22) → Your IP

Or SSH (22) → 0.0.0.0/0 (only for testing)

4. Wrong public IP

If you relaunched the instance, the IP changed.

Fix: Use the new Public IPv4 DNS from AWS.

 5. Using the wrong command

Make sure your SSH command looks like:

ssh -i "mykey.pem" ec2-user@your-public-dns.compute.amazonaws.com


These notes help me quickly fix the most common SSH problems I run into during labs.
