EC2 Connection Steps (Beginner Notes)

These are my simple notes on how to connect to an EC2 instance using SSH. I wrote this to help myself remember the commands and the flow.

1️⃣ Launch EC2

Choose Amazon Linux 2

Select instance type (t2.micro)

Make sure the correct key pair is selected

Allow SSH (port 22) in security group

2️⃣ Locate your key file

Example:
mykey.pem

Move it into a folder you remember.

3️⃣ Change key permissions

chmod 400 mykey.pem
4️⃣ Connect to the instance

Use the command provided in AWS:

ssh -i "mykey.pem" ec2-user@ec2-xx-xx-xx-xx.compute.amazonaws.com

5️⃣ If you get “Permission denied (publickey)”

Common fixes:

Wrong region

Wrong key file

Instance relaunched and needs a new key

Using the wrong username (ec2-user for Amazon Linux)

