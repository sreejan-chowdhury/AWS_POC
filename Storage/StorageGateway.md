- Acts as a bridge between on-prem apps and cloud-based storage using standard protocol and interface.
- Has 3 different types: File, Volume and Tape Gateway.

## File Gateway
- Provides a virtual file server, which allows user to store and retrieve S3 objects via standard file storage protocols ( Network FIle System (NFS) or Server Message Block (SMB))
- Embedded in the on-prem server through NFS client.
- Gateway converts these file operations into object requests on your S3 bucket.
 ![image](https://user-images.githubusercontent.com/55656762/120903310-26cd9000-c663-11eb-92fb-137f7dda4564.png)


## Volume Gateway
- Mounted to on-prem app server throught iSCSI (Internet Small COmputerr System Interface) devices.
- iSCSI devices enable us to access the network drive remotely through our system.
- The data in the drive is taken as snapshot and stored in S3. These snapshots are used to create a volume and attach them to the instance or on-prem server.
- Different configs or modes :
  1. Stored : All of the data is cached locally and is backed up by taking snapshots of the volume and storing it in S3.
![image](https://user-images.githubusercontent.com/55656762/120903291-fede2c80-c662-11eb-926e-b3cf65ab23ec.png)

  2. Cached : Frequently used data is cached locally, with all content backed up in S3 by taking snapshots in a scheduled or ad-hoc manner.
![image](https://user-images.githubusercontent.com/55656762/120903283-f1c13d80-c662-11eb-9780-79224cf948bd.png)


## Tape Gateway  
 - Provides cost effective and durable solution to archive data.
 - Mounted to on-prem app server throught iSCSI devices, which is preconfigured with tape drive and media changer.
 - Tape drive helps to perform I/O and seek permission operation on tape.
 - Media changer helps to manage the tapes in Virtual Tape Library (VTL)
![image](https://user-images.githubusercontent.com/55656762/120903271-de15d700-c662-11eb-8076-93e9256f4ee2.png)


 
