---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:
* Study Amazon Cognito identity management and automated web hosting with AWS Amplify.
* Focus on Frontend development: Integrate Cognito authentication (Login, Sign-up, JWT Tokens) directly into the app.
* Configure continuous integration and automated deployment (CI/CD) on AWS Amplify connected to GitHub.
* Review role-based access control (Student vs. Instructor workflows) across the platform with the team.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| :---: | :--- | :---: | :---: | :--- |
| 2 | - Study Amazon Cognito for user management. Instead of spending time on complex container labs (ECR/ECS Fargate) that aren't needed for the Frontend, I focused deeply on Cognito User Pool concepts. | 05/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Integrate complete authentication flows (Signup, Login, Password Recovery) into the **Aura Academic** Frontend. Handle secure JWT token storage and implement protected route guards. | 07/06/2026 | 08/06/2026 | |
| 6 | - Connect our Frontend GitHub repository to AWS Amplify, configuring CI/CD pipelines to build and deploy live updates whenever code is pushed to the main branch. | 09/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - Hold team sync to cross-test user role permissions (Student vs. Instructor access) and verify UI responsiveness across both desktop and mobile screens. | 11/06/2026 | 11/06/2026 | |

### Week 8 Achievements:

* Understood how Cognito authentication works and how to set up automated web hosting with AWS Amplify.
* Successfully integrated complete login, registration, and role authorization directly into the Frontend application.
* The **Aura Academic** web interface is now live on a secure HTTPS AWS Amplify domain, updating automatically on every Git push.
* Confirmed strict role isolation: students can only access exam rooms and their test history, while instructors can access exam management and score analytics.
