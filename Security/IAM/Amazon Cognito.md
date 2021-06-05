Provides authentication, authorization, and user management for your web and mobile apps.

 - User Pool : User Directory that provides sign-up and sign-in options
 - Identity Pool : User can use this to obtain temporary credentials to access AWS services.

## Features
 - secure, scaable and fully managed user directory.
 - uses identity management standards like OpenID Conncet, OAuth 2.0, etc
 - provides security features like MFA and ecryption of data-at-rest and in-transit
 - provides solutions to control access to backend AWS resources


## Pricing
https://aws.amazon.com/cognito/pricing/

## DEMO
1. Allow Login through Social Media, Create own login credentials, Enable email communication.

 - Login to AWS account and Select Cognito
 - choose Manage User Pools.
 - Create a User Pool. Fill out the values.
 - Create App client ID. 
 - Create SES client ID. GOTO SES. Verify a New Email Address. Verify This Email Address.
 - Back in User Pool Review Page, select MFA abd Verfication. Select `Optional`
 - Select `email` for ` Which attr do you want to verify?`
 - Create a Role and copy the ARN. Put this arn in the New role name.
 - Select the email we verifed for SES as `From email`. Use SES service.
 - Keep all other values as default. Create Pool.
 - Select `App Integration`, choose `Domain Name`. Enter unique domain name and check if available. Save
 - Select `App client Setting`. Choose ` Select All`. Choose `Cognito User Pool`.
 - Enter the `CallBack URL` (URL of page to redirect after successful sign-in)
 - Enter Sign out URL.
 - Under OAth 2.0, select `Authrozation Code Grant` and `Implicit Grant`
 - Under Allowed OAuth scopes, select all. 	  
 - Goto `UI Customization` , upload the logo and save.
 - Goto `App Client Settings` , click `Launch Hosted UI`

2. https://labrlearning.medium.com/a-detailed-look-at-aws-cognito-da19b1dd0fba