# Types
1. Managed
 - AWS Manged
 - Customer Manged

2. Inline

# Components of JSON
 - Version : 
 - Statement : 
 - Effect : 
 - Action :
 - Resource : Specifies the objects that the statement covers.
 - Principal : Specifies the identity.

## Note:
- Policies are created using `Generator` ( UI where we choose services and set permissions, and generator converts it to JSON template)
- We can directly write it in JSON too.

# Check:
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_examples.html
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_policy-summary-examples.html

an example :
> {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "FullAccess",
            "Effect": "Allow",
            "Action": ["s3:*"],
            "Resource": ["*"]
        },
        {
            "Sid": "DenyCustomerBucket",
            "Action": ["s3:*"],
            "Effect": "Deny",
            "Resource": ["arn:aws:s3:::customer", "arn:aws:s3:::customer/*" ]
        }
    ]
}

# Example 
### Create a new policy to allow a user of S3 Read and List only