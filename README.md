# 1.Scalable-Web-App-with-ALB-and-Auto-Scaling

## Project Overview
This project demonstrates a **highly available and scalable web application** using AWS services. The system automatically handles traffic spikes using Auto Scaling and distributes traffic using an Application Load Balancer.

---

## Objective
To build a fault-tolerant web application that:
- Automatically scales based on traffic
- Distributes load evenly across instances
- Ensures high availability and reliability

---

## Architecture Overview

The system is designed to handle high traffic using load balancing and auto scaling.

### Components:
- ALB (Application Load Balancer)
  - Distributes incoming traffic across multiple EC2 instances
  - Ensures high availability and fault tolerance

- Auto Scaling Group
  - Automatically adds/removes EC2 instances based on traffic

- EC2 Instances
  - Hosts the web application

- Security Groups
  - Controls inbound and outbound traffic rules

## AWS Services Used

- :contentReference[oaicite:0]{index=0} – Virtual servers to host the application
- Application Load Balancer – Distributes incoming traffic across multiple instances
- Auto Scaling Group – Automatically adds/removes EC2 instances based on demand
- Security Groups – Controls inbound and outbound traffic rules

---

## Architecture Flow
User → Application Load Balancer → Target Group → EC2 Instances (Auto Scaling Group)

1. Auto Scaling Group Setup
- Created Launch Template
- Configured minimum, maximum, and desired capacity
- Attached scaling policies
  <img width="602" height="269" alt="Picture1" src="https://github.com/user-attachments/assets/07d1109d-a8c8-45dc-8eec-52e1495da34d" />


2. Target Groups
- Created target group for EC2 instances
- Registered instances automatically via Auto Scaling

<img width="602" height="89" alt="Picture3" src="https://github.com/user-attachments/assets/283f6581-846e-4e1e-9d87-283a82a7edcb" />

3. EC2 Instances (Auto Scaling)
- Two new instances launched automatically
- Instances registered in target group
<img width="602" height="123" alt="Picture4" src="https://github.com/user-attachments/assets/337fda6c-64bb-44b9-af07-cbd933be7681" />

4. Auto Scaling Activity
- Verified scaling events in AWS console
- Confirmed instance health checks
<img width="602" height="148" alt="Picture5" src="https://github.com/user-attachments/assets/3ef5e5be-2a86-4d50-82cf-0f679bf11be9" />
<img width="602" height="103" alt="Picture2" src="https://github.com/user-attachments/assets/e5eb3814-b0e2-4d73-a094-e382930e3f56" />

  

Final Output
The application is successfully running and accessible through the **Application Load Balancer DNS**, showing proper distribution of traffic across EC2 instances.
<img width="542" height="92" alt="Picture6" src="https://github.com/user-attachments/assets/52247da5-237b-45d0-81ce-09c4494be83e" />
<img width="543" height="94" alt="Picture7" src="https://github.com/user-attachments/assets/cae6f6c9-cc53-4f4c-aaeb-382159d1e7fe" />
<img width="542" height="99" alt="Picture8" src="https://github.com/user-attachments/assets/f7ef03e0-f59c-40fc-a26a-8e73b18c3fc3" />

