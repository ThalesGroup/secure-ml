# Awesome Agentic AI Security

A curated list of open-source libraries, tools, and frameworks for securing agentic AI systems — covering guardrails, sandboxing, red teaming, observability, and policy enforcement.

> Last updated: April 2026

---

## Table of Contents

- [Guardrails & Runtime Protection](#guardrails--runtime-protection)
- [Sandboxing & Isolation](#sandboxing--isolation)
- [Policy Enforcement & Governance](#policy-enforcement--governance)
- [Red Teaming & Vulnerability Scanning](#red-teaming--vulnerability-scanning)
- [Prompt Injection Defense](#prompt-injection-defense)
- [Code Security for Agents](#code-security-for-agents)
- [Observability & Monitoring](#observability--monitoring)
- [Standards & References](#standards--references)
- [Contributing](#contributing)

---

## Guardrails & Runtime Protection

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) | NVIDIA | Programmable guardrails for LLM-based conversational systems. Uses Colang, a domain-specific language for defining conversational flows, topic boundaries, and safety constraints. Uniquely models entire conversation flows rather than just filtering individual inputs/outputs. | Apache 2.0 |
| [LlamaFirewall](https://github.com/meta-llama/PurpleLlama/tree/main/LlamaFirewall) | Meta | Open-source guardrail system for building secure AI agents. Combines PromptGuard 2 (jailbreak detection), AlignmentCheck (chain-of-thought auditing for goal misalignment), and CodeShield (static analysis for unsafe code). Used in production at Meta. | MIT |
| [Guardrails AI](https://github.com/guardrails-ai/guardrails) | Guardrails AI | Programmatic framework for validating LLM outputs using pre-built or custom validators from Guardrails Hub. Supports Python and JavaScript. Focuses on structural output validation and risk mitigation. | Apache 2.0 |
| [Invariant Guardrails](https://github.com/invariantlabs-ai/invariant) | Invariant Labs | Contextual security layer for LLM and MCP-powered AI applications. Deploys between your app and MCP servers/LLM providers for continuous steering and monitoring. Detects PII, secrets, copyright infringement, prompt injection, and harmful content. | Apache 2.0 |
| [Superagent](https://github.com/superagent-ai/superagent) | Superagent AI | Framework for building and running AI agents with safety guardrails built into the workflow. Agents operate within configurable constraints that restrict API calls, data access, and execution paths. Protects against prompt injections, data leaks, and harmful outputs. | MIT |
| [LLM Guard](https://github.com/protectai/llm-guard) | Protect AI | AI security toolkit that scans LLM inputs and outputs for security and compliance risks. Runs 15 input scanners on prompts and 20 output scanners on responses. Covers prompt injection, toxicity, PII leakage, and more. | MIT |
| [OpenGuardrails](https://openguardrails.com/) | Community | Guard agent that acts as a security proxy for AI agents, monitoring and enforcing safety policies in real-time. | MIT |

## Sandboxing & Isolation

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [OpenShell](https://github.com/NVIDIA/OpenShell) | NVIDIA | Secure-by-design runtime for autonomous AI agents. Provides kernel-level sandboxed execution environments with declarative YAML policies. Enforces defense in depth across file access, network activity, privilege escalation, and syscall filtering. Agents cannot override policies even if compromised. | Apache 2.0 |
| [OpenSandbox](https://github.com/nichochar/open-sandbox) | Community | Secure, fast, and extensible sandbox runtime for AI agents. Provides isolated execution environments for running untrusted agent code safely. | MIT |

## Policy Enforcement & Governance

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit) | Microsoft | Seven-package system (Python, TypeScript, Rust, Go, .NET) addressing all 10 OWASP Agentic AI risks. Includes **Agent OS** (policy engine with sub-ms latency, supporting YAML/OPA Rego/Cedar), **Agent Mesh** (DID-based crypto identity and inter-agent trust protocol), **Agent Runtime** (execution rings, saga orchestration, kill switch), and **Agent SRE** (SLOs, circuit breakers, chaos engineering). | MIT |

## Red Teaming & Vulnerability Scanning

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [Garak](https://github.com/NVIDIA/garak) | NVIDIA | LLM vulnerability scanner — the "nmap for LLMs." Probes for hallucination, data leakage, prompt injection, misinformation, toxicity, jailbreaks, and more. Supports Hugging Face, OpenAI, Cohere, Replicate, and custom REST endpoints. Extensible with custom probes and plugins. | Apache 2.0 |
| [PyRIT](https://github.com/Azure/PyRIT) | Microsoft | Python Risk Identification Toolkit for generative AI. Automates red teaming with customizable attacker and evaluator LLMs. Structured framework for executing OWASP Top 10 attacks against AI systems. | MIT |
| [Promptfoo](https://github.com/promptfoo/promptfoo) | Promptfoo | Open-source LLM testing and red teaming platform. Adaptive attack generation, web-based workflows, and OWASP Top 10 compliance mapping built in. Surfaces jailbreaks, prompt injections, and safety regressions pre-deployment. | MIT |
| [Giskard](https://github.com/Giskard-AI/giskard) | Giskard AI | AI testing and red teaming framework for LLMs and AI agents. Continuous security testing to detect vulnerabilities before they reach production. Supports automated test generation and compliance scanning. | Apache 2.0 |
| [Open-Prompt-Injection](https://github.com/liu00222/Open-Prompt-Injection) | Academic | Benchmark suite for prompt injection attacks and defenses. Enables implementation, evaluation, and extension of attacks, defenses, and LLM-integrated applications. | MIT |
| [CyberSecEval](https://github.com/meta-llama/PurpleLlama/tree/main/CybersecurityBenchmarks) | Meta | Cybersecurity safety evaluation benchmarks for LLMs. Tests for insecure code generation, cyberattack helpfulness, and vulnerability to prompt injection. Part of Meta's Purple Llama project. | MIT |

## Prompt Injection Defense

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [Rebuff](https://github.com/protectai/rebuff) | Protect AI | Self-hardening prompt injection detector with four-layer defense: dedicated LLM analysis, vector database of past attacks, canary token detection, and heuristic checks. Learns from previous attacks to strengthen over time. | Apache 2.0 |
| [Vigil](https://github.com/deadbits/vigil-llm) | Community | Python library and REST API for assessing LLM prompts and responses. Detects prompt injections and jailbreaks using vector similarity, YARA/heuristic rules, transformer models, prompt-response similarity, and canary tokens. | MIT |

## Code Security for Agents

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [CodeShield](https://github.com/meta-llama/PurpleLlama/tree/main/CodeShield) | Meta | Online static analysis engine for preventing generation of insecure or dangerous code by coding agents. Fast, extensible, and designed for real-time deployment in agentic pipelines. Part of LlamaFirewall. | MIT |
| [Semgrep](https://github.com/semgrep/semgrep) | Semgrep | Fast, open-source static analysis tool. While not AI-specific, widely used to scan AI-generated code for security vulnerabilities, injection flaws, and unsafe patterns. Supports 30+ languages. | LGPL 2.1 |

## Observability & Monitoring

| Project | Maintainer | Description | License |
|---------|-----------|-------------|---------|
| [Langfuse](https://github.com/langfuse/langfuse) | Langfuse | Open-source LLM engineering platform for observability, tracing, metrics, evals, and prompt management. Integrates with OpenTelemetry, LangChain, OpenAI SDK, LiteLLM, and more. 21k+ GitHub stars. | MIT |
| [LangKit](https://github.com/whylabs/langkit) | WhyLabs | Open-source text metrics toolkit for monitoring LLM and NLP applications. Extracts signals for toxicity, sentiment, text quality, relevance, and security-related patterns. Integrates with whylogs for drift detection. | Apache 2.0 |
| [OpenLLMetry](https://github.com/traceloop/openllmetry) | Traceloop | Open-source observability for LLM applications built on OpenTelemetry. Provides automatic tracing and monitoring for LLM calls, vector DB queries, and agent actions. | Apache 2.0 |

## Standards & References

| Resource | Organization | Description |
|----------|-------------|-------------|
| [OWASP Top 10 for Agentic Applications (2026)](https://genai.owasp.org/) | OWASP | First formal taxonomy of risks specific to autonomous AI agents: goal hijacking, tool misuse, identity abuse, memory poisoning, cascading failures, rogue agents, and more. |
| [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | OWASP | Industry-standard risk classification for LLM applications including prompt injection, insecure output handling, training data poisoning, and more. |
| [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence/ai-risk-management-framework) | NIST | Framework for managing risks in AI systems throughout their lifecycle. |
| [Awesome AI Security](https://github.com/ottosulin/awesome-ai-security) | Community | Curated collection of resources related to AI security — papers, tools, and guides. |

---

## Contributing

Contributions are welcome! Please submit a pull request to add new tools or update existing entries. When adding a project, please include:

- Project name and link to the repository
- Maintainer or organization
- A brief description of what it does and how it secures agentic AI
- License type
- Whether it is actively maintained
