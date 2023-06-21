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

