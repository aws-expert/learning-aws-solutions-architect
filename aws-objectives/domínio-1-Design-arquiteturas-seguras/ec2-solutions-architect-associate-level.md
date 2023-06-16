# EC2 - Solutions Architect Associate Level.

## Elastic Network Interfaces (ENI)
- logical component in a VPC that represents a virtual network card.
- the ENI can have the following attributes:
  - primary private IPv4, one one more secondary IPv4.
  - one elastic IP (IPv4) per private IPv4
  - one public IPv4
  - one or more security groups

  
- you can create ENI independently and attach them on the fly (move them) on EC2 instances for failoer.
- bound to a specific availability zone (AZ).