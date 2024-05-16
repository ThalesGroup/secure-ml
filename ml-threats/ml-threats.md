# Cyber Threats to Machine Learning

Machine learning systems are susceptible to various cyber threats, compromising their integrity and functionality. Understanding these threats is crucial for developing robust defense mechanisms. Here are two significant cyber threats to machine learning.

**![image](../images/mlt.png){ width=60%}**

## 1. Malwared ML

Malwared ML involves exploiting machine learning systems as a channel to launch attacks. This threat encompasses various malicious activities, including:

- **Infiltrating Datasets**: Injecting malware such as viruses, trojans, worms, spyware, etc., into machine learning datasets.
- **Compromising Pre-trained Models**: Embedding malicious code or payloads into pre-trained models, potentially leading to harmful outcomes.
- **Manipulating Outputs**: Altering the output of machine learning models by injecting malicious data, thereby influencing decision-making processes.

### Mitigation Strategies

To mitigate Malwared ML attacks, it is essential to:

- Implement robust data validation and sanitization techniques.
- Regularly audit and verify pre-trained models for integrity.
- Deploy anomaly detection mechanisms to identify suspicious activities within machine learning pipelines.

## 2. Adversarial ML

Adversarial ML involves targeted attacks on machine learning models, aiming to deceive or manipulate their behavior. This threat encompasses various attack vectors, including:

- **Evasion Attacks**: Crafting input data to mislead the model's predictions, leading to incorrect outputs.
- **Inference Attacks**: Exploiting vulnerabilities in the model's inference process to extract sensitive information or infer hidden patterns.
- **Data Poisoning**: Injecting malicious data during the training phase to manipulate the model's learning process and compromise its performance.

### Mitigation Strategies

To mitigate Adversarial ML attacks, it is essential to:

- Employ robust model validation techniques, such as adversarial training and model ensembling.
- Implement input sanitization and anomaly detection mechanisms to detect and mitigate evasion attacks.
- Regularly monitor model performance and behavior to detect anomalies and potential inference attacks.

These cyber threats underscore the importance of incorporating security measures at every stage of the machine learning lifecycle to ensure the reliability and trustworthiness of ML systems.