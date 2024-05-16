# Security Plan for Machine Learning Systems

## Purpose
The purpose of this security plan (SecPlan) is to establish a framework for ensuring the security, privacy, and integrity of machine learning (ML) systems within the organization. This policy outlines activities, responsibilities, and best practices to protect ML models, data, and infrastructure from unauthorized access, malicious attacks, and privacy breaches.

## Applicability
This SecPlan is applicable whenever organization employees are:
- Engaged in the internal development of a machine learning model for commercial or opensource purposes,
- Using a downloaded publicly available pre-trained model for commercial or opensource purposes,
- Utilizing the AI services provided by CSPs (Cloud Service Providers) in a Software-as-a-Service (SaaS) or Platform-as-a-Service (PaaS) model or in serverless deployment for commercial or opensource purposes (e.g. use of pre-trained models provided by the CSPs),
- Utilizing either publicly accessible or internally generated training or validation datasets.

This SecPlan is not applicable when using external Gen AI services like Copilot, ChatGPT, or Gemini. Refer to the specific security guidelines to implement for those.

## Scope
This policy applies to all employees, contractors, and third-party vendors who develop, maintain, deploy, or utilize ML systems within the organization. It encompasses all stages of the ML lifecycle, including data collection, model training, deployment, monitoring, and maintenance.

## ML SecPlan - Brief
**![image](../images/ml.png)**

* **Data Security**: It refers to securing data that can be training data, validation data, data stored in vector databases, etc.
* **Model Security**: It refers to hardening the model in both development and inference time. 
* **Platform Security**: It refers to hardening of the underlying platform where the ML model is being developed or operated, along with any associated data.
* **Security Compliance**: It refers to being compliant to both internal and external regulations, standards, and best practices as application to the Trusted AI principles.
* **Human Security**: It refers to humans being well trained, authenticated, authorized, and capable to handle security incidents around ML ecosystem.

## ML SecPlan - Goals and Techniques
|  | DATA SECURITY | MODEL SECURITY | PLATFORM SECURITY | SECURITY COMPLIANCE | HUMAN SECURITY |
| -------- | ---- | ---- | ---- | ---- | ---- |
| GOAL | Confidentiality, Integrity, Availability, Autentication, Authorization, Non-repudiation, Privacy | Integrity in Computation, Accuracy and precision in output | API security, System security (+ Cloud security), Network security | Comply with internal and external regulations | People involved are authorized and aware of security risks |
| TECHNIQUES | Encryption, Access Controls, Data backups & Recovery, Data anonymization, Data quality control, Secure data sharing, Data classification | Secure development, Input and Output validation, Model explainability, Adversarial training, Robustness testing, Monitoring and alerting, Secure deployment | Vulnerability scanning & Penetration Testing, Patch management, Access Controls, Encryption, Hardening, Secure Configuration  | Regulatory compliance, Ethical considerations, Data retention and deletion, Audit trails, Security assessments, Third-party risk management  | Training and awareness, Background checks, Incident response, Governance and oversight, Continuous monitoring |

For details, refer to [ML SecPlan - Detailed](ml-secplan-detailed.md)