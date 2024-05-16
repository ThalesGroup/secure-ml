## Secure Coding Guidelines for Machine Learning model development

Here're some of the secure coding guidelines to be followed when developing machine learning (ML) models or processing of the data required as input, irrespective of the programming language.

### Validate inputs
Machine learning models are vulnerable to attacks that exploit input validation vulnerabilities, such as data poisoning and evasion attacks. To prevent these attacks, it is important to validate inputs and sanitize them before they are used in the model.

### Validate outputs
Machine learning models are vulnerable to attacks that exploit output validation vulnerabilities, such as model replication and exfiltration. To prevent these attacks, it is important to validate outputs and sanitize them before they are sent to the requester.

### Use secure data storage
Machine learning models often rely on sensitive data, such as personally identifiable information (PII), that must be stored securely. It is important to use strong encryption and access controls to protect this data.

### Use secure algorithms
Some machine learning algorithms, such as k-means clustering or decision trees, may be vulnerable to attacks that manipulate the model's decision-making process. It is important to use algorithms that are robust against these attacks.

### Use secure data pre-processing
Pre-processing data is a critical step in machine learning, and it is important to do it securely. This may involve using secure data transformation techniques, such as differential privacy or homomorphic encryption, to prevent data leakage.
Reference: https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html

### Implement watermarking
Model weights are sensitive information that should be protected against unauthorized access or modification. This may involve encrypting the weights or using other techniques, such as model watermarking, to detect and prevent theft.

### Implement access controls
Machine learning models should only be accessible to authorized users or processes. It is important to implement access controls, such as authentication and authorization, to prevent unauthorized access to the model.

### Log every input request and output response
Every data that is input to the machine learning model, the processing action within the model neural network, and the resulting output (before and after activation function or encoding) must be logged for SIEM purposes.