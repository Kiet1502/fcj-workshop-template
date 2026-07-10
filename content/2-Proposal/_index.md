---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# PROPOSAL  
## AURAACADEMIC  
### Online Examination and AI Proctoring Platform on AWS  

---

### 1. Executive Summary  
AuraAcademic is an online examination platform integrated with AI proctoring (Powered by Bedrock & Rekognition/YOLOv8) to ensure fairness and transparency for remote exams. The system leverages YOLOv8 models for real-time cheating detection via webcam. By combining AWS architecture (CloudFront, ECS Fargate, EC2 GPU Spot) with Serverless and Managed Services, AuraAcademic delivers an automated proctoring solution with high accuracy at a fraction of the cost of traditional live proctoring, ideal for educational institutions.

---

### 2. Problem Statement  
**Current Problems:**  
Existing online exam platforms lack effective automated proctoring mechanisms, making academic dishonesty easy to commit. Commercial AI proctoring solutions on the market (such as Proctorio, Respondus) often come with expensive licensing fees, complex integration, and demand high bandwidth or massive server resources.

**Solution:**  
AuraAcademic solves this challenge by building a comprehensive end-to-end system:  
- **Frontend (React.js):** Statically hosted on Amazon S3 and distributed globally via CloudFront for a smooth user experience.  
- **Backend Core API (Spring Boot):** Hosted on ECS Fargate (or EC2) to process exam logic, submission workflows, and authentication.  
- **AI Proctoring (YOLOv8/Rekognition):** Running on EC2 GPU instances (utilizing Spot Instances to save up to 70% in costs) to analyze live video streams (detecting looking away, leaving frame, unauthorized persons, etc.).  
- **Video Streaming:** Webcam video streams sent via WebRTC/WebSocket to the AI service for real-time anomaly detection during the exam.  
- **Authentication & Security:** Utilizing Amazon Cognito for user login, combined with AWS WAF to protect APIs.  

**Benefits & Highlights:**  
The system automatically detects cheating behaviors, minimizing manual proctoring effort. By leveraging Spot Instances for AI processing and flexible Serverless/Container architecture, operational costs are dramatically optimized for universities and educational organizations.

---

### 3. Solution Architecture  
AuraAcademic adopts a Microservices architecture on AWS, clearly decoupling Core API services from AI Processing pipelines.

**AWS Services Utilized:**  
- **Amazon S3 & CloudFront:** Global storage and high-speed delivery of the React.js Frontend web application.  
- **Amazon Cognito:** Identity management and user authentication (students, instructors) via JWT tokens.  
- **ALB (Application Load Balancer):** Routing REST API requests to ECS or EC2 Backend services.  
- **Amazon ECS Fargate:** Running containerized Spring Boot Backend core API services.  
- **Amazon EC2 (Spot - GPU):** Running Python AI services to process student camera streams.  
- **AWS WAF:** Web Application Firewall protecting APIs against DDoS attacks and common web exploits.  
- **Amazon SES:** Sending automated email notifications, registration confirmations, and violation alerts to students.  
- **VPC, Public/Private Subnets & NAT Gateway:** Ensuring secure network isolation across all services.  
- **External Services:** MongoDB Atlas (Database), Google Gemini API (Automated question generation / Bedrock assistance).  

**Component Design:**  
- **Web Interface:** Students take exams and activate monitoring webcams; Instructors manage exam papers and view violation logs.  
- **Core API:** Processes exam business logic, submissions, and role verification via JWT, connecting directly to the Database.  
- **AI Engine:** Receives camera streams via WebSocket/WebRTC, detects anomalies using YOLOv8, and pushes real-time alert updates back to the Core API.

---

### 4. Technical Implementation  
**Implementation Phases (Planned 3-Month Internship):**  
- **Month 1 (Setup & Design):** VPC architecture analysis, MongoDB Atlas database setup, YOLOv8/Bedrock model preparation.  
- **Month 2 (Backend & AI Development):** Spring Boot API programming, Cognito integration, AI service deployment on EC2 Spot.  
- **Month 3 (Refinement & Deployment):** React.js UI development, S3 + CloudFront + WAF + ALB infrastructure setup, load testing, and documentation finalization.  

**Technical Requirements:**  
- **Frontend:** React.js, Tailwind CSS, Axios, WebRTC client.  
- **Backend:** Spring Boot, Spring Security, MongoDB Atlas connection.  
- **AI Processing:** Python, FastAPI, YOLOv8/OpenCV/Rekognition, real-time video stream processing.  
- **AWS Infrastructure:** S3, CloudFront, Cognito, ECS Fargate, EC2 Spot, ALB, WAF, SES, VPC.

---

### 5. Roadmap & Milestones  
- **Weeks 1-2:** System architecture analysis, VPC network design, and data flow mapping.  
- **Weeks 3-5:** Core API development with Spring Boot and Cognito authentication setup.  
- **Weeks 6-8:** Frontend UI construction and online exam workflow integration with AI Proctoring.  
- **Weeks 9-10:** AWS infrastructure deployment (ECS Fargate, EC2 Spot, CloudFront, WAF) and end-to-end testing.  
- **Weeks 11-12:** Performance optimization, cost evaluation, and final internship report drafting.

---

### 6. Budget Estimation  
Using AWS pricing model with Spot Instances and Serverless strategies for a production environment (~100 concurrent students):  
- **Frontend (S3 + CloudFront):** ~$1.00 USD/month (Free Tier / very low data transfer cost).  
- **ECS Fargate Spot (Backend):** ~$3.00 - 5.00 USD/month.  
- **EC2 GPU Spot (AI Engine - g4dn.xlarge):** ~$0.15 - 0.20 USD/hour (activated only during exams, estimated ~$8.00 - 12.00 USD/month).  
- **NAT Gateway (Optional / or VPC Endpoints):** ~$10.00 - 15.00 USD/month.  
- **Application Load Balancer (ALB):** ~$16.00 USD/month.  
- **MongoDB Atlas:** ~$0.00 USD/month (Free Tier M0 cluster).  
- **SES & WAF:** ~$2.00 USD/month.  
👉 **Total Estimated Budget:** Approximately **30 - 50 USD/month** (AWS Credits can be used to fully cover practical lab expenses).

---

### 7. Risk Assessment  
**Risk Matrix:**  
- **Spot Instance Sudden Interruption:** Impact: Medium | Likelihood: High | *Note: Configure Auto Scaling Group or automatic fallback to On-Demand.*  
- **High Camera Stream Latency:** Impact: Medium | Likelihood: Medium | *Note: Optimize frame resolution and configure efficient WebSocket/WebRTC protocols.*  
- **Billing Surge:** Impact: High | Likelihood: Low | *Note: Set up CloudWatch Billing Alarms and automatically shut down GPU EC2 instances immediately after exam sessions.*  

**Mitigation Strategies:**  
- **Spot Instances:** Configure Auto Scaling Groups with Multi-AZ and multi-instance type strategies, automatically falling back to On-Demand if Spot capacity is unavailable.  
- **Camera Latency:** Send only critical keyframes or compress video streams to just enough resolution for accurate AI detection.  
- **AWS Cost Control:** Set AWS Budgets alerts and configure Lambda automation to stop AI processing servers during non-exam hours.

---

### 8. Expected Outcomes  
- **Technical Improvements:** Deliver an automated exam monitoring solution with high accuracy using AWS AI, rapid response latency, and robust security.  
- **Practical Value:** Enhance skills in automation, Cloud Microservices architecture design, and cost-optimized system operations for educational environments.