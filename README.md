# LLM Guardrail & Observability Service

A deployable service that sits between an application and an LLM (Google Gemini via Vertex AI) and checks every input and output for security-related failures. Two core guardrails: prompt injection detection (input) and PII leakage detection (input & output). Each request is logged as a typed event; a monitoring layer tracks trigger rates, latency, and input drift; a periodic evaluation job measures detector performance against a red-team test set.

Why: Every organization rolling out LLMs in production needs guardrails and observability. The project demonstrates the full chain from evaluation design through serving to operational monitoring.