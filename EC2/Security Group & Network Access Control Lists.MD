These are types of Firewalls to protect resources on AWS.

Security Groups are VPC specific.

Security Group :
Applied at Instance level. on one or more instances
Supports Allow Rules only
Stateful
Evaluates all Rules
Applies to an instance only if associated with a group

NACL :
Applied at Subnet Level
Supports allow and deny rules
Stateless
Processes Rules in Order
Automatically applies to all instances in the subnets it is associated with.





#######################
Inside VPC there are Network ACL and Security Group.

By default communication is allowed only within the Security Group.


## FIREWALLS

Stateful : If the firewall has an inbound rule . e.g traffic from a particular port . Then outbound rule isn't required.
          Security group

Stateless : Will check for Rule for both inbound and out bound connections So both rules are required.
            Network ACL
