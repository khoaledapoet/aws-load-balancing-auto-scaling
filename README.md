# AWS Scalable Web Architecture with Load Balancer and Auto Scaling

## Project Overview
This project demonstrates how to build a scalable and highly available web architecture on AWS.  
The system automatically distributes traffic across multiple EC2 instances using a load balancer and scales resources dynamically based on demand.

The infrastructure ensures high availability, fault tolerance, and monitoring for a web application environment.

## Architecture

![Architecture](architecture/architecture.png)

### Architecture Components

- Amazon VPC
- Public and Private Subnets
- NAT Gateway
- Application Load Balancer
- Auto Scaling Group
- EC2 Instances
- CloudWatch Monitoring

## Technologies Used

- AWS EC2
- AWS Auto Scaling
- AWS Elastic Load Balancing
- AWS CloudWatch
- Apache Benchmark (ab) for load testing

## System Workflow

1. User sends request from the Internet
2. Request goes through Application Load Balancer
3. Load Balancer distributes traffic to EC2 instances
4. Auto Scaling automatically launches or terminates instances based on CPU usage
5. CloudWatch monitors system metrics

## Screenshots

### Load Balancer Configuration
![LoadBalancer](screenshots/load-balancer.png)

### Auto Scaling Group
![AutoScaling](screenshots/auto-scaling-group.png)

### CloudWatch Monitoring
![CloudWatch](screenshots/cloudwatch-monitor.png)

### Load Testing Result
![LoadTest](screenshots/load-test-result.png)

## Load Testing

The system was tested using Apache Benchmark to simulate multiple concurrent users.

Example command:
ab -n 1000 -c 50 http://<load-balancer-dns>
Result:  
The system automatically scaled EC2 instances when the traffic increased.

## Project Structure


aws-auto-scaling-load-balancer
│
├── architecture
│ └── architecture.png
│
├── screenshots
│ ├── load-balancer.png
│ ├── auto-scaling-group.png
│ ├── cloudwatch-monitor.png
│ └── load-test-result.png
│
├── report
│ └── aws-auto-scaling-load-balancer-report.pdf
│
└── README.md


## Full Report

For detailed implementation steps, refer to the project report:

[View Full Report](report/aws-auto-scaling-load-balancer-report.pdf)

## Author

Nguyễn Đăng Khoa  
Cloud Computing / Network Engineering Student