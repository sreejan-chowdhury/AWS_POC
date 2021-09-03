## Amazon Machine Image :
Add softwares to an image and use that image...makes life easy...
Alternative softwares TO AMI: puppet, chef
It is not free...
What ever is in the base instance used for making the AMI, will be available in the new instance that have used the AMI.

1.Launch EC2
2. Connect to EC2
3. Create a file ... echo "Welcome " > somefile.txt
4. From Dashboard ... Right Click and Create Image.
5. use the image to launch a EC2 instance...connect to it and check if the file is present...


The Snapshot is saved in EBS..
