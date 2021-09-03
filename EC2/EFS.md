Elastic File System....

Difference with EBS
1. EBS is like local HardDisk...but EFS is like Network Drive.
2. EBS is faster.
3. EBS and EC2 have to be in the AZ.
4. EBS is RAW Storage, so we have to format it.
5. SAN for EBS ... NAS for EFS
6. for EBS we need to provide initial capacity but for EFS we don't need to put any capacity..it will auto increase and decrease size.


For EFS access :
1. We need to create a Security Group to allow inbound NFS protocol.
2. We have to mount the EFS to the EC2.
3. we have to create mount target for the EC2 AZ we want to mount to. We can have Mount Targets for each AZ we want to connect to.

## Example
 1. Create 2 EC2 instances...
 2. Create Security Group : Allow inbound NFS : port 2049
 3. GOTO EFS : Create the EFS
 4. GOTO both EC2 and install nfs-common:
    sudo su
    apt-get update
    apt-get install nfs-common -y

    #create directory and mount
    mkdir ~/efs-mount-dir
    mount -t nfs -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport <EFS IP>:/ ~/efs-mount-point
    cd ~/efs-mount-point
 5. create file from one EC2 in the Folder and access it from the other EC2.
