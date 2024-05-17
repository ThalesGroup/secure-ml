## ML Security Plan - Security Requirements

For context, please refer to the [earlier page](ml-secplan.md) before proceeding with this content.

### Data Security

ID | TECHNIQUE | ACTIVITY
-------- | ---- | -----
DS1 | Encryption  | Sensitive data must be encrypted both in transit and at rest to protect against unauthorized access. Project teams must implement strong encryption algorithms, such as AES or RSA, and ensure that keys are managed securely.
DS2 | Access Controls | Project teams must implement strict access controls to ensure that only authorized personnel have access to sensitive data. This includes measures such as user authentication, role-based access control, and multi-factor authentication.
DS3 | Data classification, backups and recovery | Project teams must classify data based on its sensitivity labels, implement regular data backups and have a disaster recovery plan in place to ensure that data can be restored in the event of a data breach or other disaster.
DS4 | Data anonymization | Project teams must anonymize data by removing personally identifiable information (PII) or by using techniques such as data masking or tokenization. This will help protect the privacy of individuals while still allowing ML models to be trained on the data.
DS5 | Data quality control | Project teams must implement processes to ensure the quality and integrity of the data used for training and testing AI models. This includes measures such as data file and content validation, and antivirus scans.
DS6 | Secure data sharing | When sharing data with third parties, project teams must ensure that appropriate security measures are in place, such as secure data transfer protocols, data usage agreements, and data access controls.

### Model Security
ID | TECHNIQUE | ACTIVITY
-------- | ---- | -----
MS1 | Secure development | Project teams must implement version control for AI models, just as they would for software code, to track changes and ensure the integrity of the model. This includes measures such as code repositories, branching, code review, and the associated development environment.
MS2 | Input/output validation | Project teams must validate the inputs and outputs of AI models to ensure that they are accurate and reliable. This includes measures such as data validation, data normalization, and data transformation to get rid of untrusted and dangerous inputs.
MS3 | Model explainability | Project teams must ensure that AI models are explainable and transparent, meaning that the logic and decision-making process of the model can be understood by humans. This includes measures such as feature importance analysis, model visualization, and threat modeling the AI model.
MS4 | Adversarial training & Robustness testing | Project teams must perform robustness testing to ensure that AI models are resilient to malware such as virus, worm, spyware, or trojan and adversarial attacks, such as input perturbation, extraction, inference or data poisoning. This includes measures such as scanning for malware, adversarial training, robustness metrics, and model hardening (source code vulnerability fixes and mitigating or avoiding the use of vulnerable third-party libraries or components used in the model development).
MS5 | Monitoring and alerting | Project teams must monitor AI models in production to detect anomalies or unexpected behavior. This includes measures such as logging, monitoring, and alerting.
MS6 | Secure deployment | Project teams must deploy AI models securely, ensuring that appropriate security measures are in place, such as secure communication protocols, access controls, authentication, and reverse engineering protection mechanisms.

### Platform Security
ID | TECHNIQUE | ACTIVITY
-------- | ---- | -----
PS1 | Vulnerability scanning | Project teams must perform vulnerability scanning and penetration testing to identify and mitigate vulnerabilities in the infrastructure and systems used for AI and ML. 
PS2 | Patch management | Project teams must implement a robust patch management process to ensure that software and firmware updates are installed promptly to address known security vulnerabilities.
PS3 | Access controls | Project teams must implement access controls to ensure that only authorized personnel have access to the infrastructure and systems used for AI and ML. This includes measures such as user authentication, role-based access control, and multi-factor authentication.
PS4 | Encryption | Project teams must use encryption to protect data in transit and at rest. This includes measures such as TLS for secure communication and full-disk encryption for storage.
PS5 | Network hardening | Project teams must implement network security measures, such as firewalls, intrusion detection/prevention systems, and network segmentation, to protect against network-based attacks.
PS6 | Hardware security | Project teams must ensure that hardware used for AI and ML, such as GPUs and TPUs, is secure and protected against tampering or physical attacks.
PS7 | Secure Configuration | Project teams must ensure ML systems are configured securely, following best practices for network, systems, and applications hardening in cloud or on-prem. 

### Security Compliance
ID | TECHNIQUE | ACTIVITY
-------- | ---- | -----
SC1 | Regulatory compliance | Project teams must ensure that their AI and ML systems comply with relevant regulations and standards, such as HIPAA, GDPR, PCI-DSS, or ISO 27001. This includes measures such as data protection, security controls, and privacy requirements.
SC2 | Ethical considerations | Project teams must consider the ethical implications of their AI and ML systems, particularly in areas such as bias, fairness, and accountability. This includes measures such as bias mitigation techniques, ethical frameworks, and algorithmic transparency.
SC3 | Data retention and deletion | Project teams must implement policies and procedures for data retention and deletion to comply with regulatory requirements and ensure the privacy of individuals. This includes measures such as data minimization, data anonymization, and data destruction.
SC4 | Audit trails | Project teams implement audit trails to track data access and usage, particularly in regulated industries where compliance with regulations is mandatory. This includes measures such as logging, monitoring, and reporting.
SC5 | Security assessments | Project teams must perform security assessments of their AI and ML systems to identify potential vulnerabilities and ensure compliance with regulatory requirements. This can include measures such as security risk assessments, security audits, and compliance assessments.
SC6 | Third-party risk management | Project teams must ensure that third-party vendors and partners comply with regulatory requirements and security standards, particularly when they have access to sensitive data or systems used for AI and ML.

### Human Security
ID | TECHNIQUE | ACTIVITY
-------- | ---- | -----
HS1 | Training and awareness | Project teams must provide training and awareness programs for employees and stakeholders to ensure that they understand the risks and best practices associated with AI and ML security. This includes measures such as security training, awareness campaigns, and phishing simulations.
HS2 | Background checks | Project teams must conduct background checks on employees and contractors who have access to sensitive data or systems used for AI and ML, particularly in regulated industries or government agencies.
HS3 | Incident response | Project teams must have an incident response plan in place to handle security incidents related to AI and ML, such as data breaches or cyber-attacks. This includes measures such as incident management, forensics communication plans and associated people to be involved.
HS4 | Governance and oversight | Project teams must establish governance and oversight structures to ensure that AI and ML systems are developed, deployed, and used in a secure and ethical manner. This includes measures such as compliance frameworks, security dashboards, and risk management processes and waivers.
HS5 | Continuous monitoring | Project teams must implement continuous monitoring of AI and ML systems to detect and respond to security incidents in real-time. This can include measures such as logging, monitoring, and analytics.

For implementation details of the above requirements, refer to [ML security guidelines](guidelines/ml-secplan-guidelines.md).