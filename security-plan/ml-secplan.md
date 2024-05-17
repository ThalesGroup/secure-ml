# Security Plan for Machine Learning Systems

## Purpose
The purpose of this security plan (SecPlan) is to provide a policy framework for ensuring the security, privacy, and integrity of machine learning (ML) systems within the organization. This policy outlines activities, responsibilities, and guidelines to protect ML models, data, and infrastructure from unauthorized access, malicious attacks, and privacy breaches.

## Applicability
This SecPlan is applicable whenever organization employees are:
- Engaged in the internal development of a machine learning model for commercial or opensource purposes,
- Using a downloaded publicly available dataset or pre-trained model for commercial or opensource purposes,
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

For details, refer to [ML SecPlan with security requirements](ml-secplan-detailed.md)


## Exceptions
Exceptions to this ML Security Policy may be granted in certain circumstances, subject to a thorough review and approval process. Exceptions will be considered on a case-by-case basis and should follow the principle of maintaining an acceptable level of risk while ensuring the security and privacy of ML systems.

## Exception Request
- Any employee or team seeking an exception to this policy must submit a formal exception request to the designated authority.
- The exception request should include a detailed justification for the proposed deviation from the policy, along with supporting evidence, risk assessment, and mitigating controls, if applicable.

## Review and Approval Process
- The designated authority responsible for reviewing exceptions (DIS-ITE-Central Security) will assess the request in consultation with relevant stakeholders, including the ML solutoin owner, development team, legal department, and data privacy officers.
- The review process will consider the potential impact on security, privacy, compliance, and the organization's risk tolerance.
- The designated authority will communicate the decision regarding the exception request to the requesting party in a timely manner.

## Documentation and Tracking
- Approved exceptions will be documented, including the rationale for the exception, mitigating controls (if any), and any additional safeguards implemented.
- The exceptions and their associated documentation will be tracked and periodically reviewed to ensure continued compliance and evaluate the need for ongoing exceptions.

## Periodic Review
- All exceptions granted under this policy will be subject to periodic review to assess their ongoing necessity and appropriateness.
- The designated authority will conduct reviews at least annually or whenever there are significant changes in the ML system, security landscape, or regulatory requirements.

## Policy Updates
This exception section of the policy will be periodically reviewed and updated to incorporate lessons learned, emerging best practices, and changes in regulations or organizational requirements.

Please note that exceptions to this policy should be considered exceptions rather than the norm, and the organization should strive to adhere to the policy's guidelines and best practices. Exceptions should be granted sparingly and with a clear understanding of the associated risks and mitigation strategies.