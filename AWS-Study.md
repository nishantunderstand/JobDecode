EC2

AMI (Amazon Machine Image) is a template used to launch EC2 instances.
AMI is a preconfigured image used to create EC2 instances.

EC2 → Virtual Machine in AWS
AMI → Template used to create EC2
Instance Type → CPU + RAM configuration

Elastic IP : Static IP Address
Normally, when an EC2 instance is stopped and started, its public IP may change.


What is User Data?
User Data is a startup script executed automatically when an EC2 instance launches.


On-Demand vs Reserved vs Spot

Stop vs Terminate
Stop
VM shuts down
Can start again
Data on EBS remains

Terminate
VM permanently deleted
Cannot restart

Can a terminated EC2 instance be restarted?

How do you connect to EC2?

How do you deploy a Spring Boot Application on EC2?
Steps
Launch EC2
Install Java
Copy JAR file

What happens if EC2 crashes?
Single EC2
Multiple EC2


How do you troubleshoot a slow EC2?
Check CPU : top
Check Memory : free -m
Check Disk :  df -h
Check Application Logs  : tail -f app.log
Check JVM : jstack , jmap


Your Spring Boot Application Gets 10x Traffic. What Will You Do?