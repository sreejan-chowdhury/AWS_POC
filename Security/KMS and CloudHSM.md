## Access Keys:
 - Used to verify identity of the user or an Application.
 - Consists of access key ID and a secret key.

## Key Mangement System (KMS)
It is a managed encryption service that enables user to eadily encrypt user data.
Provides highly available key storage, management, and auditing solution to encrypt data across AWS serices.

 - Creates keys with unique alias and description
 - Allows to Import your own keys
 - Defines which IAM users and roles can manage keys
 - Defines which IAM users and roles can use keys to encrypt and decrypt data
 - Audit use of keys by inspecting logs in `AWS CloudTrail`

Developers can you AWS SDKs with AWS KMS support to easily use and protect encryption keys.
We can use it to verify data encryption across the app where it is used and stored.


## CloudHSM
Hardware Security Model. 
The entire cryptography key lifecycle from provisioning, managing, and storring to disposal or archiving the keys occurs in HSM.
Used to support DB encryption, Digital Rights Management, Public Key Infrastucture, authentication and authorization, document signing, and transaction processing.
 
 - The user creates a CloudHSM Cluster.
 - Clusters comtain multiple HSM instances, spread across multiple AZs in a Region.
 - HSM instances in a cluster are automatically synchronized and load balanced.
 - User gets dedicated, single tenant access to each HSM instance.
 - Each HSM instance appears as a network resoirce in your VPC.
 - Adding and Removing HSMs from cluster is done through AWS CLoudHSM API or AWS CLI.
 - After creating and initializing a CLoudHSM cluster, configure a client on EC2 instance that allows user's app to use the cluster over secure, authenticated network connection.

![image](https://user-images.githubusercontent.com/55656762/120082542-3daf3800-c0e1-11eb-8248-fd5f111fda4b.png)
