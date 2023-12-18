# RDS Overview

- RDS stands for relational database service.
- it's a managed database service for DB use a SQL.
- allows you to create database in the cloud that are managed by AWS.
  - Postgress
  - MySQL
  - MariaDB
  - Oracle
  - Microsoft SQL Server
  - Aurora  Database.

## Advantages of using RDS database service.
- RDS is managed service
  - automating provisioning, OS patching.
  - continuous backup and restore to a specific timestamp.
  - monitoring dashboards
  - read replication for improved read performance.
  - multi az setup for disaster recovery.
  - maintenance windows for upgrade
  - scale capabilities.
  - storage backed by EBS volumes (gp2).
- but you cannot SSH into the database instances.

## RDS -Storage Auto Scaling
- helps you increase storage on your RDS DB instance.
- RDS detects you are running out of free database storage, it scales automatically.
- maximum storage threshold
  - automatically modify storage if
    - free storage is less than 10% of allocated storage.
    - 6 hours have passed since las modification.
    - low storage lasts at least 5 minutes.





