# High Availability and Scalability: ELB & ASG
- there are two kinds of scalability
  - vertical scalability
  - horizontal scalability (elasticity)
- scalabilty is linked but different to high availability.

## Vertical Scalability
- vertical scalability means increasing the size of instance
- for example, your application runs on a t2.micro.
- scaling the application vertically means running it on a t2.large.
- RDS, ElastiCache are services that can scale vertically.

### CNCF definition of vertical scalability
O escalonamento vertical, também conhecido como “escalonamento para cima e para baixo”, é uma técnica em que a capacidade de um sistema adiciona CPU e memória aos nós individuais à medida que a carga de trabalho aumenta. Digamos que você tenha um computador de 4GB de RAM e queira aumentar sua capacidade para 16GB de RAM, escalar verticalmente significa mudar para um sistema de 16GB de RAM.

## Horizontal Scalability
- horizontal scalability means increasing the number of instances/systems for your application.
![text](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/image1.png)

- horizontal scaling implies distributed systems.
- this is very common for web applications/modern aplications
- it's easy to horizontally scale thanks the clod offering such as Amazon EC2.

## High Availability
- high availability ussialy goes hand in hand with the horizontal scaling.
- high availability means running your application/system in at leasr 2 data centers (== availability zones).
- the goal of high availability is to survive a data center loss
- the high availability can be passive (for RDS multi AZ for example)
- the high availability can be active for horizontal scaling.

## High Availability and Scalability for EC2
- vertical scaling: increase instance size (= scale up/down)
  - from: t2.nano
  - to: u-l2tbl.metal
- horizontal scaling: increase number of instances (=scale out/in)
  - Auto Scaling Group
  - Load Balancer
- high availability: run instances for the same application across multi AZ
  - Auto Scaling Group multi AZ
  - Load Balancer multi AZ.


## What is load balancing?
- load balances are servers that forward traffic to multiple servers (e.g., EC2 instances) downtream.
![text](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/image2.png)

## Why use a load balancer?
- spread load across multiple downtream instances
- expose a single point of access (DNS) to your application
- semlessly handle failures of downstream instances
- do regular health checks to your intances
- provide SSL termination (HTTPS) for your websites.
- enforce stickness with cookies.
- high availability across zones
- separate public traffic from private traffic.
- 


