Threat Detection Service that continously monitors for any malicious activiyt to protect customer's AWS account and workloads.

Once Amazon GuardDuty is enabled, it automatically monitors for 
 - Anomalous API activity 
 - Potentially unauthorized deployments and compromised instances 
 - Reconnaissance by attackers

## GuardDuty is free for 30 days once we enable it. 

### Consists of : 
	- Data Sources 
	- Findings
	- Detector
	- Suppression Rule
	- Trusted IP List
	- Threat List

https://aws.amazon.com/premiumsupport/knowledge-center/guardduty-cloudwatch-sns-rule/


# Use Case:
 1. https://aws.amazon.com/blogs/security/how-to-use-amazon-guardduty-and-aws-web-application-firewall-to-automatically-block-suspicious-hosts/

 2. Check the UseCases directory.


# Examples and Reading:

Setting up GuardDuty

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_settingup.html

Working with trusted IP lists and threat lists

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_upload-lists.html

Severity Levels

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_findings.html

GuardDuty findings

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-ec2.html
https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-s3.html
https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-iam.html

Creating custom responses to GuardDuty findings with Amazon CloudWatch Events

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_findings_cloudwatch.html

Visualizing Amazon GuardDuty findings

https://aws.amazon.com/blogs/security/visualizing-amazon-guardduty-findings/

Tester with commands

https://github.com/awslabs/amazon-guardduty-tester

How you can use Amazon GuardDuty to detect suspicious activity within your AWS account

https://aws.amazon.com/blogs/security/how-you-can-use-amazon-guardduty-to-detect-suspicious-activity-within-your-aws-account/ 