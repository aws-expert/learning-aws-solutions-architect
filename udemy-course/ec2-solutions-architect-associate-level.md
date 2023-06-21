# EC2 - Solutions Architect Associate Level.

## Elastic Network Interfaces (ENI)
- logical component in a VPC that represents a virtual network card.
- the ENI can have the following attributes:
  - primary private IPv4, one or more secondary IPv4.
  - one elastic IP (IPv4) per private IPv4
  - one public IPv4
  - one or more security groups
- you can create ENI independently and attach them on the fly (move them) on EC2 instances for failoer.
- bound to a specific availability zone (AZ).

## EC2 Hibernate
- we know can stop, terminate instances.
  - stop - the data disl (EBS) is kept intact in the next start
  - terminate - any EBS volumes (root) also set-up to be destroyed is lost.

- on start, the following happens:
  - first start - the OS boots and the EC2 user data scripts run
  - following start - the OS boots up.

### EC2 Hibernate
- introducing EC2 hibernate
  - the in-memory (RAM) state is preserved
  - the instance boot is much faster (the OS is not stopped/restarted)
  - under the bood - the RAM state is written to a file in the root EBS volume
  - the root EBS volume must be encrypted.

### Uses cases
- long-running processing
- saving the RAM state
- services that take time to initialize.

### EC2 Hibernate - Good to know
- supported instance families - C3, C4, C5, I3, M3, M4, R3, R4, T2, T3
- instance RAM size - must be less than 150GB
- instance size - not supported for bare metal instances
- AMI - Amazon LINUX 2, LINUX AMI, Ubuntu, RHEL, CentOS, Windows
- root volume - must be EBS encrypted, not instance store and large
- available for on-demand, reserved and spot instances.
- an instance can NOT be hibernated more than 60 days.










