## Security Code-Review Guidelines for Machine Learning model development

Here're some of the security related code-review guidelines to be followed after developing machine learning (ML) models or processing of the data required as input, irrespective of the programming language.

### Review for data validation
Check that the code is properly validating the input data to prevent security vulnerabilities like SQL injection or cross-site scripting.

### Check for secure storage
Ensure that the code is using secure storage practices for any sensitive data used by the model, such as personally identifiable information (PII), and that this data is not being exposed or stored in an insecure manner.

### Review model architecture
Review the model architecture and algorithms to ensure they are secure and robust against attacks like adversarial examples.

### Review data pre-processing
Check the pre-processing code to ensure that data is being pre-processed securely and that no sensitive information is being leaked.

### Review input data
Review the input data to ensure it is not malicious or adversarial and does not contain any sensitive information that should not be processed by the model.

### Review output data
Check the output data to ensure that it is being produced securely and does not contain any sensitive information.

### Review access controls
Check the code for proper access controls, such as authentication and authorization, to ensure that only authorized users or processes can access the model.