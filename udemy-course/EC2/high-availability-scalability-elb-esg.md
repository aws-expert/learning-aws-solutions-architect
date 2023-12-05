# High Availability and Scalability (ESG & ASG)

- there are two kinds of scalability
  - vertical scaling
  - horizontal scaling (elasticy)
- scalability is linked but different to high availability.

## Vertical scaling
- vertically scalabity means increase the size of the instance.
- for example, your application runs on a t2.micro.
- scaling that application vertically means running it on a t2.large.
- is more common is database systems (distributed systems)
- RDS, ElastiCache, are services that can scale vertically.

![Alt text](image.png)

## Horizontal scaling
- increasing the number of instances/systems for your application.
- horizontal scaling implies distributed systems.
- this is very common for web applications/modern applications.
- its easy to scale horizontally thanks the cloud offering such as Amazon EC2.

![Alt text](image-1.png)

## High Availability.
- usually goes hands in hand with horizontal scaling.
- means running your application in at least 2 data centers (== availability zones).
- the goal of high availability is to servive a datacenter loss.
- can be passive (for RDS Multi AZ for example)
- can be active (for horizontal scaling).

## High Availability and Scalability for EC2
- vertical scaling, inscrease instance size (scale up and dows)
- horizontal scaling, increasing the number of instances (scale out scale in).
- 