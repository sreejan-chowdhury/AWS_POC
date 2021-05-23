# IAM Components 
### IAM Users:
 - Individual who has set of permissions. Users have permanent credentials to directly interact with AWS resources.

### IAM Groups:
 - Collection of IAM users. 

### IAM Roles:
 - Deines set of [ermissions for making AWS service request.

### IAM Policies:
 - Specify those permissions that you want to acquire. Can be attached to User, Group or Roles.     
 
# Create User
 - Login as root or admin.
 - Goto IAM
 - Select User. Add User `sreejan-test` / `********` . Select change password on next sign in.
 - Create a Group or add to one already created. I created a new group `S3AccessGroup` and attached `S3FullAccess` policy 
 - Add a Tag if you want to.
 - Review and Create.

 Got a sign in URL : https://sreejan-aws-test-root.signin.aws.amazon.com/console
 - Login and change the password. `*****@**`

# Access Advisor
 - Access Advisor reports activity for services and EC2, IAM, Lambda, and S3 management actions. 


> NOTE : Only Root user has access to Billing & Cost Management Dashboard.

# To Study
### ABAC : Attribute Based access Control
  - Done through Tags. Tag the user and tag the instance.

  https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_attribute-based-access-control.html
  https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_attribute-based-access-control.html
  https://www.youtube.com/watch?v=aO6j68USsfY
