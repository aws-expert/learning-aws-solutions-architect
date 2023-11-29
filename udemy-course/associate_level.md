# Private vs Public IP
- IPv4 is the most common formt used online.

## Private vs Public IP (Differences)
- Public IP
  - means the machine can be identified on the internet (WWW)
  - must be unique across the whole web
  - can be geo-located easily.

- Private IP
  - sss
  - the IP must be unique across the private network.
  - machines connected to WWW using a NAT + internet gateway (a proxy)
  - only a specific range if IP address can be used as private IP.

- Elastic IPs
  - when you stop and start an EC2 instance it can change its public IP address.
  - fixed public IP in the  EC2 instance.
  - 


# Elastic Network Interfaces (ENI)
- logical component that represents a virtual network card.
- the ENI can have the following properties
  - primary IP address (IPV4) or more IP addresses (IPV4)
  - one elastic IP address one per private ipv4 address.
  - one public ipv4 address.
  - one or more security groups.


