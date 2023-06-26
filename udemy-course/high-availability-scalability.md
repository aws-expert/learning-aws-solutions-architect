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

