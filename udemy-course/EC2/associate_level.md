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

# EC2 Hibernate
- introducing the EC2 hybernate
  - the memmory RAM state is preserved.
  - the instance boot is faster (the OS is not stopped and restarted).
  - ec2 is the default implementation.

## Uses Cases
- long running processing
- saving the ram state
- services that take a long time to initialize.

## EC2 Hibernate - Good to know
- supported instance families - C3, C4, C5, I3, M3, M4, R3, R4, T2, T3
- instance RAM size - must be less than 150GB
- instance size - not supported for bare metal instances
- AMI - Amazon LINUX 2, LINUX AMI, Ubuntu, RHEL, CentOS, Windows
- root volume - must be EBS encrypted, not instance store and large
- available for on-demand, reserved and spot instances.
- an instance can NOT be hibernated more than 60 days.





