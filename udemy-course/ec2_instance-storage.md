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

![aws-image](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/aws11.png)

