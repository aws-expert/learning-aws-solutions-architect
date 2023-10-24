# EC2 Fundamentals

## Amazon EC2 
- EC2s is one of the most popular of aws offering
- EC2 = elastic compute cloud = infrastructure as a service
- it mainly consists in the capability of:
  - renting virtual machines (EC2)
  - storing data on virtual drives (EBS)
  - distributing load across machines (ELB)
  - scaling the services using an auto-scaling group (ASG).  

## EC2 sizing & configuration options
- operating system (OS), LINUX, Windows or Mac.
- how much compute power & cores (CPU)
- how much random-access memory (RAM)
- how much storage space:
  - network-attached (EBS & EFS)
  - hardware (EC2 instance store)
- network card: speed of the card, public IP address.
- firewall rules: security group
- bootstrap script (configure at first launch): EC2 use data.

## EC2 User Data
- it is possible to bootstrap out instances using an EC2 User Data script.
- bootstraping means lauching commands when a machine starts
- that script is only run once at the instance first start.
- EC2 user data is used to automate boot tasks such as:
  - installing updates
  - installing software
  - downloading common files from the internet.

## EC2 Instance Types - Overview
- you can use different types of ec2 instances that are optimized for different use cases.
- AWS name convention:
  - **m5.2xlarge**
- m: instance class
- 5: generation
- 2xlarge: size within the instance class

