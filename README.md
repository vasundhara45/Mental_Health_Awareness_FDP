# Agentic AI for Mental Health Awareness & Suicide Prevention

An empathetic, proactive, and safe Agentic AI system built to address the growing global challenge of mental health distress — depression, anxiety, and suicidal ideation — through early detection, RAG-grounded guidance, and explainable risk classification.

> ⚠️ **Disclaimer:** This system is **not a substitute for professional medical advice, diagnosis, or treatment**. If you or someone you know is in crisis, please contact a licensed mental health professional or a local emergency/helpline service immediately.

---

## Problem Statement

Mental health issues such as depression, anxiety, and suicidal thoughts are growing worldwide. Stigma, lack of awareness, and limited access to timely help prevent many individuals from seeking support. Traditional systems are often **reactive**, leaving gaps in early detection and preventive care.

## Objective

Build an Agentic AI-powered Mental Health Awareness & Suicide Prevention Agent that:

1. **Promotes Awareness & Education** — shares accessible resources on mindfulness, coping strategies, and self-care.
2. **Enables Early Detection (RAG)** — uses Retrieval-Augmented Generation to identify distress signals in conversational input.
3. **Provides Empathetic Support** — listens actively and responds with empathy, with clear disclaimers that it is not a substitute for professional care.
4. **Classifies Risk by Severity** — routes conversations into Low, Moderate, High, and Critical risk tiers for tier-appropriate responses.
5. **Is Explainable by Design** — surfaces the reasoning behind every risk classification, not just the output.

---

## Architecture Overview

```
User input (chat message)
        │
        ▼
Resource ingestion ──▶ Knowledge base (RAG)
        │                  awareness & helplines
        ▼
Distress detection agent
   (identifies risk signals)
        │
        ▼
   Smart router
 (routes by severity)
        │
 ┌────┬────┬────┬────┐
 Low  Mod  High  Critical
 └────┴────┴────┴────┘
        │
        ▼
 Empathetic response
  (with safety disclaimer)
        │
        ▼
 Explainability layer
  (why this risk level)
        │
        ▼
   Response delivered
```

**Pipeline stages:**

| Stage | Function |
|---|---|
| **User input** | Captures the incoming chat message |
| **Resource ingestion → Knowledge base (RAG)** | Ingests awareness content and helpline information into a retrievable knowledge base |
| **Distress detection agent** | Analyzes the conversation for early distress/risk signals |
| **Smart router** | Uses an LLM to classify the message into a severity tier |
| **Severity tiers (Low / Moderate / High / Critical)** | Branches the flow so each risk level gets a differently calibrated response strategy |
| **Empathetic response** | Generates a supportive, tier-appropriate reply with an embedded safety disclaimer |
| **Explainability layer** | Surfaces the rationale behind the assigned risk level |
| **Response delivered** | Final output returned to the user |

---

## Tech Stack

- **Orchestration:** LangFlow
- **Foundation Models:** IBM Granite models via IBM watsonx.ai
- **Retrieval:** RAG (Retrieval-Augmented Generation) over a curated mental health knowledge base
- **Knowledge Sources:** Awareness/education content, mindfulness & coping resources, verified helpline information

---

## Key Features

- 🧩 **Multi-agent pipeline** — detection, routing, response, and explanation handled by distinct agents rather than a single monolithic prompt
- 🎯 **Severity-tiered routing** — Low / Moderate / High / Critical classification drives response strategy
- 📚 **RAG-grounded answers** — responses are retrieved from a curated knowledge base, reducing hallucinated or unsafe advice
- 🔍 **Built-in explainability** — every risk classification comes with a rationale, not just a label
- 🛡️ **Disclaimer-by-design** — every empathetic response includes an explicit "not a substitute for professional advice" notice
- 🏢 **Enterprise-grade foundation** — built on IBM watsonx.ai with IBM Granite models for governed, reproducible pipelines

---

## Novelty & Uniqueness

- **Multi-agent risk pipeline** instead of a single LLM handling detection, routing, and response in one prompt
- **Severity-tiered response strategy** that mirrors real-world triage rather than a flat, one-size-fits-all reply
- **RAG-grounded safety** — recommendations are retrieved from curated sources, not generated purely from model memory
- **Explainability as a first-class component**, not an afterthought
- **Safety disclaimers embedded into the pipeline itself**, not left to prompt engineering alone

---

## Future Scope

- Integration with wearables & physiological signals (heart rate, EDA) for richer, real-time distress detection
- Voice and multilingual support for broader accessibility
- Stress forecasting to predict and pre-empt crisis points before they occur
- Consent-based human escalation to counselors, helplines, or emergency contacts for Critical-risk cases
- Caregiver/clinician feedback loops for continuous model improvement
- Privacy-preserving, on-device or federated deployment for sensitive data
- Clinical validation and alignment with digital health regulatory frameworks
- Multi-tenant, enterprise-scale deployment across schools, universities, and workplace wellness programs

---

## Project Status

This is a **hackathon prototype** built to demonstrate the feasibility of an agentic, explainable, RAG-grounded approach to mental health awareness and early risk detection. It is not a validated clinical tool.

---

## License

Add your license here (e.g. MIT, Apache 2.0).
