---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Aura Academic | Smart Exam Engine  
## Next-Generation AI-Powered Online Examination & Proctoring Platform on AWS Cloud  

*Live Production & Demonstration Link:* [Aura Academic Frontend AWS S3 Hosting](http://aura-academic-fe-2024.s3-website-ap-southeast-1.amazonaws.com/vi/)

---

### 1. Executive Summary  
**Aura Academic (Smart Exam Engine)** is a revolutionary smart online assessment and examination platform developed by our team to solve critical challenges regarding academic integrity, proctoring security, and workflow optimization for universities, high schools, training institutes, and educators. By deeply integrating cutting-edge Artificial Intelligence (**AI Proctoring**, **Generative AI**) with modern **AWS Cloud & Serverless** architecture, Aura Academic delivers high scalability, ultra-low latency, and cost-effective operations.  

### 2. Problem Statement  
* **Current Challenges:**  
  - **Lack of Supervision:** Online exams often suffer from vulnerabilities to cheating, including impersonation, unauthorized material consultation, leaving the camera frame, or switching browser tabs/applications during exams.  
  - **Time-Consuming Exam Creation:** Teachers spend countless hours manually extracting, formatting, and structuring question banks from raw textbook files (DOCX, PDF).  
  - **Infrastructure Overload:** Traditional Learning Management Systems (LMS) often experience network bottlenecks or server crashes during peak concurrent exam sessions, and lack comprehensive analytical post-exam reporting.  

* **Our Breakthrough Solution - Aura Academic:**  
  - **AI Camera / Real-Time AI Proctoring:** Leverages Computer Vision to monitor facial recognition in real-time, detecting multi-face presence, candidate swapping, leaving the frame, or suspicious audio noise within a **Secure Room** environment.  
  - **Exam Builder / High-Speed Automated Generation:** Integrates Large Language Models (**LLMs / Generative AI**) to automatically parse learning documents (DOCX/PDF) and generate structured, multi-difficulty exam matrices with a single click.  
  - **Auto Report & Comprehensive Analytics:** Features instant automated grading, transparent **Audit Logs**, and dynamic score distribution charts that allow educators to evaluate question quality and student performance.  

* **Benefits & Return on Investment (ROI):**  
  - Reduces preparation and grading time for educators by up to **80%**.  
  - Ensures **99%** transparency, fairness, and security across all online examinations.  
  - Leverages AWS Cloud-Native & Serverless architecture (Amazon S3, CloudFront, Lambda, Bedrock...) to eliminate initial upfront server costs, paying only for actual operational throughput (**Pay-as-you-go**).  

### 3. Solution Architecture & AWS Cloud Integration  
**Aura Academic** is built upon a robust, highly resilient Serverless architecture on Amazon Web Services (AWS), capable of supporting thousands of concurrent test-takers without managing physical servers:  

* **Frontend Hosting & CDN:**  
  - The modern web interface (built with Next.js/React, featuring smooth Light/Dark mode transitions) is statically exported and hosted on **Amazon S3**.  
  - Distributed globally via **Amazon CloudFront** edge network for lightning-fast delivery and built-in DDoS protection (Live URL: `http://aura-academic-fe-2024.s3-website-ap-southeast-1.amazonaws.com/vi/`).  

* **AI & Machine Learning Layer:**  
  - **Amazon Bedrock:** Provides advanced Foundation Models (FMs/LLMs) powering the **Exam Builder** module to analyze study materials, generate multiple-choice questions, and provide detailed answer explanations.  
  - **Amazon Rekognition:** Processes live video and image streams from student webcams (**AI Proctoring**), automatically identifying and flagging potential violations or suspicious behaviors.  

* **Serverless Backend Layer:**  
  - **AWS Lambda & Amazon API Gateway:** Powers all backend business logic (room management, connection verification, submission handling, score calculation) as fully managed serverless microservices.  
  - **Amazon DynamoDB:** Sub-millisecond NoSQL database storing question banks, real-time room status, student responses, and detailed Audit Logs.  
  - **Amazon S3 (Data Storage):** Securely stores raw exam source documents and captured image evidence of exam violations.  

* **Security & Identity:**  
  - **Amazon Cognito:** Manages identity verification, authentication, and Role-Based Access Control (RBAC) across Educators, Students, and School Administrators.  

### 4. Technical Implementation & End-to-End Workflow  
* **Aura Academic's Comprehensive 4-Step Workflow:**  
  1. **Exam Creation (Exam Builder):** Educators upload source documents or select existing question banks; AI automatically recommends structured exam matrices.  
  2. **Room Configuration (Secure Room):** Educators create secure exam sessions, customize proctoring rules (camera/microphone enforcement, tab-lock), and distribute secure access codes.  
  3. **Live Exam & AI Supervision (AI Proctoring):** Students enter the secure room; AI continuously monitors the session, tracking connection stability and automatically recovering exam states if interruptions occur.  
  4. **Post-Exam Analytics (Auto Report):** Immediately upon submission, the system calculates final scores and generates detailed analytical reports and violation logs with photographic proof.  

### 5. Roadmap & Implementation Milestones (Aligned with 11-Week AWS Internship)  
- **Phase 1 (Weeks 1 – 3):** Requirement analysis, modern UI/UX design, and static Frontend deployment on **Amazon S3 + CloudFront**.  
- **Phase 2 (Weeks 4 – 7):** Research and integration of AWS AI/ML services (**Amazon Bedrock** for automated question generation, **Amazon Rekognition** for webcam proctoring).  
- **Phase 3 (Weeks 8 – 10):** Development of Serverless Backend (**AWS Lambda, API Gateway, DynamoDB**), Secure Room session management, and CI/CD pipelines.  
- **Phase 4 (Week 11 & Beyond):** Load testing, architectural documentation, blog contributions to the AWS Study Group, and real-world deployment across partner educational institutions.  

### 6. Infrastructure Budget Estimation (AWS Cloud)  
By maximizing Serverless architecture and **AWS Free Tier / Credits**, monthly operational costs remain highly optimized:  
- **Amazon S3 & CloudFront (Frontend hosting & CDN):** ~$1.50 USD/month.  
- **AWS Lambda & API Gateway (Backend API):** ~$0.50 USD/month (well within millions of free tier requests).  
- **Amazon DynamoDB (NoSQL Database):** ~$1.00 USD/month (On-Demand capacity mode).  
- **Amazon Bedrock & Rekognition (AI Services):** ~$5.00 – $15.00 USD/month (depending on question generation frequency and concurrent proctored students).  
- **Total Estimated Cost for Lab & Mid-Scale Production:** **~$8.00 – $18.00 USD/month**, achieving more than 85% cost savings compared to traditional Dedicated Servers or VPS hosting.  

### 7. Risk Assessment & Mitigation Strategies  
- **Risk of Network Interruption:** The system features local caching and browser storage (Local Storage / IndexedDB) that automatically saves answers locally and syncs immediately upon network re-establishment without data loss.  
- **Risk of False AI Flags:** AI acts as a smart flagging and alerting assistant; final disciplinary decisions always remain with human educators, backed by time-stamped image and log evidence to ensure fairness.  

### 8. Expected Outcomes & Long-Term Value  
* **Technical Advancement:** Fully replaces manual examination, question creation, and grading workflows with an automated, low-latency, highly secure cloud solution on AWS.  
* **Long-Term Impact:** Lays the foundation for a scalable Educational Technology (EdTech) ecosystem capable of supporting hundreds of schools and learning institutions nationwide.jects.