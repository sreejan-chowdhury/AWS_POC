## Does Runtime Workload distribution like:

Asymmetric : Larger worloads are assigned to resources with higher capacity.

Workload Prioritization : Schedule, queue, discard and distribute workloads based on priority.

Content-Aware : Based on request content.


# Elastic Load Balancer 

It is the Load Balancing service by AWS.

1. ELB routes traffic efficiently accross multiple registered targets based on different routing algos.
2. We can configure a load balancer to accept incoming traffic by specifying one or more listeners.
3. Target inclues (in multiple AZ) : EC2, Lambda, COntainers, Range of IP
4. Monitors the health of registered targets and routes traffic only to healthy ones.

## Types


1. Application LB

Best suited for Load Balancing http and https traffic and provides advanced request routing. Supports Websockets too.

Components:
- Listener : Conenction req from client are checked by listener using configured ports and protocols. Can add one or more listeners.
- Rules : Routing rules are defined for Listener. Determines how to route to targtes
- Target Groups : Routes req to one or more registered targets. A target can be registered with multiple target groups.
- Health Checks : Can be configured on a per target group basis. Performed on all targets registered with target groups. Supports both http and https health checks.

2. Network LB

For LB of TCP traffic where extreme performance is required. Layer 4. 
e.g : Say we are hosting an application in AWS for third party access. The third party needs to whitelist the application based on IP.

Feature :
- Static IP address for each AZ
- Ideal for handling TCP and UDP
- Source/ Remote address preservation
- Supports TLS termination
- Provides dynamic host port mapping
- supports LB to multiple ports on the same instance
- Support for Route53 DNS failover
- Supports long lived TCP connections

3. Classic LB

Provides basic LB across multiple EC2 instances and operates at both request level and connection level. Handles multiple protocols.
Supports both Iternet and Internal LB.

### E.G :
1. Create 2 EC2 instances
2. On both instances install apache:
sudo apt-get update
sudo apt-get install apache2

NOTE : change the inbound rules to allow 80 access

3. 
Create a Classic Load Balancer
Create a Security Group to be accessed on 80 port for all.
Configure Health Check.
Add the Ec2 instances.

4. Get the LoadBalancers Public DNS and access it.
By default it is Round Robin.



