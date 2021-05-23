# IAM Role
 - Better way of managing security and access than sharing/storing Access Keys.
 - It is generally attached to the AWS resource we plan to use.

# S3 Access Demo
 ### RBAC EXAMPLE
 - Create an S3.
 - GOTO :IAM Roles --> Create Role.
 - Since we are trying to access the S3 through an EC2 instance, select EC2.
 - Attach the appropriate Policy. e.g AmazonS3FullAccess
 - Tag is optional.
 - Give a name to the role
 - Create an EC2 and attach this Role to the EC2 instance. We can also attach it to an existing EC2.
 - Connect to the EC2 and check if you can access the S3 buckets. e.g: aws s3 ls