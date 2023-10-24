# What's an EBS volume??
- ane EBS volume (slastic block store) volume is a network drive you can attach to your instances while they run.
- it allows your instances to persist data, even after their termination.
- they can only be mounted to one instance at a time
- they are bound to a specific availability zone
- analogy: think of them as network USB stick

# EBS volume
- it's a network drive (not a physical drive)
  - it uses the network to communicate the instance which means there might be a bit of latency
  - it can be detached from an EC2 instance and attached to another one quickly
- it's locked to an availability zone (AZ)
  - an EBS volume is us-east-1 a cannot be attached to us-east-1b
  - to move a volume across you first need to snapshot it.

# EBS - delete on termination attribute
- controls the EBS behaviour when an EC2 instance terminates.
  - by default the root EBS volume is deleted (attributed enabled)
  - by default any other attached EBS volume is not deleted
- this can be controlled by the AWS console/AWS CLI
- use case: preserve the root volume when instance is terminated.

# EBS Snapshots
- make a backup (snapshot) of your EBS volume at point in time
- not necessary to detach volumeto to do a snapshot but recommended.
- can copy snapshots across AZ or region.

#![aws-image](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/aws11.png)

## EBS Snapshots Features
- EBS snapshot archive
  - move a snapshot to an archive tier that is 75% cheaper.
- recycle Bin for EBS snapshots
- fast snapshots restore (FSR)
  - force full initialization of snapshot to have no latency on the first use


# AMI Overview
- AMI = amazon machine image
- AMI are a customization of an EC2 instance
  - you add your own software, configuration, operating system
  - faster boot, configuration time because all your software is pre-package.
- AMI are built for a specific region (and can be copied across regions)
- you can launch EC2 instances from:
  - a public ami: AWS provided
  - your own AMI: you make and maintain them yourself
  - an AWS markplace AMI: an AMI someone else made.
  

## AMI Process (from an EC2 instance)
- start an EC2 instance and customize it
- stop the instance (for data integrity)
- build an AMI - this will also create EBS snapshots.
- launch instances from other AMI's

# EC2 Instance Store
- EBS volumes are network drives with good but limited performance
- if you need a high-performance hardware disk, use EC2 iunstance store.
  - better I/O performance
  - EC2 instance store lose their storage if they are stopped
  - good for byffer, cache, scratch, temporary content
  - risk of data loss if hardware fails.
  - backups and replication are your responsability

## EBS Volume Types
- EBS volumes come in 6 types.
  - gp2/gp3 (SSD): general purpose SSD volume that balances price and performance
  - io I/io 2 (SSD): highest performance SSD volume for mission-critical low-latency
  - st I (HDD): low cost HDD volume designed for frequently accessed.
  - sc I (HDD): lowest cost HDD volume designed for less frequently accessed workloads.
- EBS volumes are characterized in size, throughput, IOPS (I/O Ops Per Sec)
- when in doubt always consult the AWS documentation
- only gp2/gp3 and io 1/io2 cvan bse used as boot volumes.

## EBS Volume Types Use-cases
### General Purpose SSD
- cost effective storage, low-latency
- system boot volumes, vitual desktops, development and test environments.
- 1 GIB - 16 TiB
- gp3
  - baseline of 3000 IOPS
  - can increase IOPS up to 16000.
- gp2:
  - small gp2 volumes can burst IOPS
  - size of the volume and IOPS are linked
  - 3 IOPS per GB means at 5334 GB

### Provisioned IOPS (PIOPS) SSD
- critical business applications with sustained IOPS performance
- or applications that need more than 16000 IOPS
- supports EBS multi-attach.


### Hard Disk Drives (HDD)
- cannot be a boot volume
- 125GiB to 16TiB
- throughput optimized HDD
- cold HDD
  - for data that is infrequently accessed.
  - scenarios where lowest cost id important
  - max throughput 250MiB/s - max IOPS 250.

## EBS Multi-Attach - io/io2 family
- ttach the same EBS volume to multiple EC2 instances in the same AZ.
- each instance has full read and write permissions to the high performance volume
- use case  
- up to 16 EC2 instances at a time
- must use a file system thats cluster-aware.

### EBS Encryption
- when you create an encrypted EBS volume you get the following.
  - 

















