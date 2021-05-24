# Types
1. Managed
 - AWS Manged
 - Customer Manged

2. Inline

- Policies are created using `Generator` ( UI where we choose services and set permissions, and generator converts it to JSON template)
- We can directly write it in JSON too.

# Components of JSON
 - Version : 
 - Statement : 
 - Effect : 
 - Action :
 - Resource : Specifies the objects that the statement covers.
 - Principal : Specifies the identity.

# Check:
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_examples.html
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_policy-summary-examples.html

an example :
> 
{
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
 - GOTO : IAM Policy : Create Policy
 ![image](https://user-images.githubusercontent.com/55656762/119302661-18a26b80-bc82-11eb-9f90-7b34efdfcdad.png)
 
 - Select the service we want to add policy for. e.g S3
  ![image](https://user-images.githubusercontent.com/55656762/119303111-d168aa80-bc82-11eb-8c40-3ebc6f418cdf.png)

 - Add the ARN of the bucket we want to set this policy to.
  ![image](https://user-images.githubusercontent.com/55656762/119303206-fd842b80-bc82-11eb-8cfc-35802eaa674d.png)
 
 - We can also add the specific object we want to give access to.
 - Create a name and Finish.
 - Attach this Policy to a USER to test.  
