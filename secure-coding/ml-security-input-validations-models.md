## Security related input validation guidelines on Machine Learning model development and operations

Here are Python code examples and ML algorithms for implementing security-related input validation rules for LLMs. Please note that the code provided is just example reference and not to be used as-is.

*Disclaimer: Thales does not endorse the use of any specific Python library. The mention of such libraries is solely for illustrative purposes and informational use.*

### Prompt Injection Scanner
```
from llm_guard.input_scanners import PromptInjection
from llm_guard.input_scanners.prompt_injection import MatchType
 
scanner = PromptInjection(threshold=0.5, match_type=MatchType.FULL)
sanitized_prompt, is_valid, risk_score = scanner.scan(prompt)
 
#More info available at https://llm-guard.com/input_scanners/prompt_injection/
```

### PII Detection (Anonymize)
```
from llm_guard.input_scanners import Anonymize
from llm_guard.input_scanners.anonymize_helpers import BERT_LARGE_NER_CONF
 
scanner = Anonymize(vault, preamble="Insert before prompt", allowed_names=["John Doe"], hidden_names=["Test LLC"],
                    recognizer_conf=BERT_LARGE_NER_CONF, language="en")
sanitized_prompt, is_valid, risk_score = scanner.scan(prompt)
 
#More info available at https://llm-guard.com/input_scanners/anonymize/
```

### Intent Detection
```
import transformers
 
classifier = transformers.pipeline("zero-shot-classification", model="facebook/bart-large-mnli")
 
def detect_harmful_intent(prompt):
    # Generate labels for potential harmful intents
    labels = ["hate speech", "discrimination", "personal attack"]
    results = classifier(prompt, labels)
 
    # Analyze results to determine if intent is harmful
    # ...
 
#more content filtering
import profanity_filter
 
def filter_toxic_content(prompt):
    filtered_prompt = profanity_filter.censor(prompt)
    return filtered_prompt
```

### Anomaly Detection
```
from sklearn.neighbors import LocalOutlierFactor
 
def detect_anomalies(prompts):
    # Represent prompts as numerical vectors (e.g., using TF-IDF)
    # ...
 
    # Train an outlier detection model
    model = LocalOutlierFactor()
    model.fit(prompts)
 
    # Detect unusual prompts
    outliers = model.predict(prompts)
    return outliers
```

### Input Sanitization
```
import re
 
def sanitize_input(text):
    # Remove harmful content
    clean_text = re.sub(r"[\w\d]*@[\w\d.]*", "", text, flags=re.IGNORECASE)  # Remove email addresses
    clean_text = re.sub(r"https?://[^\s]+", "", text)  # Remove URLs
    # ... Add more patterns as needed
 
    # Correct errors (e.g., using a spell checker library)
    # ...
 
    # Normalize text (e.g., lowercase, remove extra spaces)
    clean_text = clean_text.lower().strip()
 
    return clean_text
```

### Length Restrictions
```
def enforce_length_restrictions(text, max_length=100):
    if len(text) > max_length:
        return False
 
    # Restrict special characters (e.g., using a regular expression)
    # ...
 
    return True
 
#Can also apply regex. Ref: https://llm-guard.com/input_scanners/regex/
```

### Format Validation
```
def validate_format(prompt):
    # Check for expected structure (e.g., question-answer format)
    if not prompt.startswith("Question:"):
        return False
 
    # Validate metadata (e.g., using a schema validator)
    # ...
 
    return True
 
#data type validation
def validate_date_format(date_string):
    try:
        datetime.datetime.strptime(date_string, "%Y-%m-%d")
    except ValueError:
        raise ValueError("Invalid date format.")
```

### Adversarial Example Detection
```
# Implementation depends on the specific adversarial detection method
# Explore research papers and libraries for available techniques
# One example library to use is https://github.com/SeldonIO/alibi-detect
 
#various code examples are available at https://github.com/SeldonIO/alibi-detect/tree/master/doc/source/examples
```

### Rate Limiting
```
import time
 
rate_limit = 10  # Maximum prompts per minute
last_prompt_time = 0
 
def enforce_rate_limit():
    global last_prompt_time
    current_time = time.time()
    if current_time - last_prompt_time < 60 / rate_limit:
        raise TimeoutError("Rate limit exceeded.")
    last_prompt_time = current_time
```

### Blacklisting and Whitelisting
```
blacklisted_words = ["hate", "violence", "discrimination"]
whitelisted_words = ["love", "peace", "respect"]
 
def check_prompt_against_lists(prompt):
    for word in prompt.split():
        if word in blacklisted_words:
            raise ValueError("Prompt contains blacklisted word.")
        elif word not in whitelisted_words:
            print("Warning: Prompt contains word not in whitelist.")
```

### Human-in-the-Loop Validation (for highly sensitive business usecases)
```
# No specific code example; this involves integrating a human review process
```

### Other validations
- Content Safety
    - Gender Bias
    - Racial Bias
    - Profanity
    - Toxicity
    - Sentiment
    - Input Output Relevance
- Security Measures
    - Malicious URL detector
    - URL reachability
    - Regex
    - Invincible Text
    - Secrets
    - Code Detection
- Privacy Protection
    - Special PII Detection
    - Anonymize
    - Fact-checking
    - Hallucination
    - Alignment to goals
- Content Access Control
    - Block competitor
    - Ban topics
    - Allowed list
- Content Analysis
    - Language detection
    - Sentiment analysis

### Note
* Adapt these examples to your specific ML models and use cases.
* Combine multiple techniques for robust defense.
* Continuously evaluate and update validation strategies.
* Stay informed about advancements in adversarial defense.