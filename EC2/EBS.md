#Elastic Block Store
30 GB free for a year..
Max size of disc is 16TB
EC2 and EBS have to be in same AZ

Incase the space is over :
1. Extend
2. Add another disk


By Default 8GB is attached.

## EXAMPLE 
1. Launch an EC2 Instance.
2. EBS --> Volumes
3. Connect to EC2 .... to find number of disks attached use : sudo fdisk -l
4. Goto the EBS / Volume Dashboard. Creat a VOlume in the same region and AZ.
5. To Attach....select the New Volume...Action...Attach..
6. mkfs <new device name from sudo fdisk -l> ..to format before using
7. mount it to a particular folder.
    mkdir /mnt/disk100
    mount <device name from sudo fdisk -l> /mnt/disk100
    ... this connects the device to the folder...to make changes to the new disk added, make change sin the Folder that is attached to the device.


8. If we terminate the EC2 instance...the default EBS ( generally 8GB ) is removed..but the addition new one is still present. We have to remove it manually.
    To use it ... we can attach it to some other EC2 in the same AZ.
    NOTE : do not format, as it will remove the  data.



Provides Persistent block storage volumes for EC2 Instances in cloud. Auto replication within availability zone.
  e.g : Big data analytics , DBs
  Provides Point in time Snapshots. We can use this snapshots to create new EC2 instances.

  Volume types : SSD backed -- for transactional workload e.g DBs and Boot Volumes.
                HDD Backed --- for throughput intensive like Map Reduce and Log Processing.
    1. IOPS SSD (io1) :
    2. Gp SSD (gp2)
    3. Throughtput Optimized HDD (st1)
    4. Cold HDD (sc1) : lowest cost
    5. Data Lifecycle Manager : Snapshot scheduler.
    6. Elastic Volumes : dynamic scaling, tune performance. : By using Amazon CloudWatch with AWS Lambda you can automate volume changes to meet the changing needs of your applications.
    7. Snapshots :
    8. Optimised Instances :
    9. Availability :
    10. Encryption :


## Check
https://tutorialsdojo.com/amazon-ebs/