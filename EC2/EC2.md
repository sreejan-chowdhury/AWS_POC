# Elastic Compute Cloud

Each instance is like a virtual machine.

## Types
  - On Demand : Instances provided on demand. Pay only for EC2 instances we use. No upfront changres.
  - Reserved : Capacity reservation for EC2 instancec is made prior. For customers with predictable workloads. Payment option are `all upfront`, `partial upfront` or `no upfront`. 75% cheaper than On-Demand instances. Prices varies with AZs.
  - Spot : Bid on a price for an instance. Suitable for workloads which are not critical and are tolerant of interruption. E.g Analytics companies run the services at 12am when other companies aren't using the EC2 services and the prices are less.


## Different types of IP addresses it can obtain:

1. Public IP :
  Lost when Instance is stopped.
  Only when you are in a public subnet.
  No Charge.
  Associated with private IP address on the instance.
  Can't be moved between Instances.


2. Private IP :
  Retained when the instance is stopped.
  Used in Public and Private Subnets.


3. Elastic IP :
  Static Public IP address. Similar to Public IP but it is not lost.
  You are charged if not used. Since IPv4 is address are scarce.
  Associated with a private IP address on the instance.
  Can be moved between instances and Elastic Network Adapters.


  To allow Private Subnets to connect to Internet we need to have a NAT ( Network Address Translation) gateway in Public subnet.
  The public subnet will communicate with the internet using the Internet Gateway.

## KEY PAIR
A key pair consists of a public key that AWS stores, and a private key file that you store.
Together, they allow you to connect to your instance securely.
For Windows AMIs, the private key file is required to obtain the password used to log into your instance.
For Linux AMIs, the private key file allows you to securely SSH into your instance.


### Create EC2
  1. Create a simple EC2 instance
  2. Create the Key Pair and download it
  3. Connect to instance :
      MAC : Select the instance. Click on Connect. It will give the instructions.
        .e.g:
        Open an SSH client.
        Locate your private key file. The key used to launch this instance is AWS Dummy Prj1.pem
        Run this command, if necessary, to ensure your key is not publicly viewable.

        chmod 400 AWSDummyPrj1.pem
        Connect to your instance using its Public DNS:

        ec2-65-2-37-239.ap-south-1.compute.amazonaws.com
        Example:

        ssh -i "AWSDummyPrj1.pem" ec2-user@ec2-65-2-37-239.ap-south-1.compute.amazonaws.com



## LAUNCH TEMPLATE
Create a Template based on requirement and use it to launch.


## NOTE
The Key Pair files created to access the EC2 are REGION specific.


