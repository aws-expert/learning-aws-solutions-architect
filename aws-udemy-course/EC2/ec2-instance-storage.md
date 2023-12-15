# EC2 Instance Storage

## EBS vs EFS Elastic Block Storage
- EBS volumes...
  - connect into one instance
  - are locke at the availability zone level.

- To migrate from an EBS volume to another AZ
  - take a snapshot of the.
  - restore the snapshot on the AZ.
  - EBS backups are use IO and shouldnt run them while your application is handling.
  
- Root EBS volumes of instance get terminated by default if the EC2 gets terminated.

