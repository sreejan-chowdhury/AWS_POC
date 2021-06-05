- Acts as a bridge between on-prem apps and cloud-based storage using standard protocol and interface.
- Has 3 different types: File, Volume and Tape Gateway.

## File Gateway
- Provides a virtual file server, which allows user to store and retrieve S3 objects via standard file storage protocols ( Network FIle System (NFS) or Server Message Block (SMB))
- Embedded in the on-prem server through NFS client.
- Gateway converts these file operations into object requests on your S3 bucket.

## Volume Gateway
- Mounted to on-prem app server throught iSCSI (Internet Small COmputerr System Interface) devices.
- iSCSI devices enable us to access the network drive remotely through our system.
- The data in the drive is taken as snapshot and stored in S3. These snapshots are used to create a volume and attach them to the instance or on-prem server.
- Different configs or modes :
  1. Stored : All of the data is cached locally and is backed up by taking snapshots of the volume and storing it in S3.
  2. Cached : Frequently used data is cached locally, with all content backed up in S3 by taking snapshots in a scheduled or ad-hoc manner.


## Tape Gateway  
 - Provides cost effective and durable solution to archive data.
 - Mounted to on-prem app server throught iSCSI devices, which is preconfigured with tape drive and media changer.
 - Tape drive helps to perform I/O and seek permission operation on tape.
 - Media changer helps to manage the tapes in Virtual Tape Library (VTL)
 
