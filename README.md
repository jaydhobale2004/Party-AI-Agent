[README_PARTY_AI_AGENT.md](https://github.com/user-attachments/files/26058875/README_PARTY_AI_AGENT.md)
# PARTY-AI-AGENT

A notebook-based **AI agent prototype** built with **smolagents**, **Hugging Face InferenceClientModel**, and **Langfuse** to explore simple agent workflows for party planning tasks such as playlist suggestions, menu selection, and task timing.

## Overview

This project is an early-stage applied AI experiment focused on agent-based task orchestration. Instead of solving a traditional machine learning prediction problem, it explores how an AI agent can combine tools, search, and lightweight reasoning to help plan a themed party.

The notebook includes examples of:

- music recommendation support
- menu suggestion based on party type
- simple time-planning logic for preparation tasks
- custom tool definitions
- web search integration
- Langfuse-based tracing / observability setup

## Tech Stack

- **Python**
- **smolagents**
- **Hugging Face Hub / InferenceClientModel**
- **DuckDuckGo Search Tool**
- **Langfuse**
- **OpenTelemetry**
- **Jupyter Notebook / Google Colab**

## What the Agent Does

The notebook demonstrates several small agent tasks, including:

- searching for playlist ideas
- generating a menu for different party styles
- estimating readiness time based on preparation tasks
- testing custom tools for themed planning support

This makes the project a good introductory prototype for understanding how tool-using agents work.

## Repository Contents

```text
PARTY-AI-AGENT/
├── PARTY_AGENTS_FOR_WAYNE.ipynb
└── README.md
```

## How to Run

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install smolagents ddgs huggingface_hub opentelemetry-sdk opentelemetry-exporter-otlp openinference-instrumentation-smolagents langfuse
   ```
3. Configure authentication securely using environment variables for any required API or platform credentials.
4. Open the notebook:
   ```bash
   jupyter notebook PARTY_AGENTS_FOR_WAYNE.ipynb
   ```
5. Run the notebook cells step by step.

## Important Security Note

Do **not** store API keys, tokens, or tracing credentials directly inside the notebook before publishing the repository. Use environment variables or a local `.env` file that is excluded from version control.

Example pattern:

```python
import os

LANGFUSE_PUBLIC_KEY = os.getenv("LANGFUSE_PUBLIC_KEY")
LANGFUSE_SECRET_KEY = os.getenv("LANGFUSE_SECRET_KEY")
LANGFUSE_HOST = os.getenv("LANGFUSE_HOST", "https://cloud.langfuse.com")
HF_TOKEN = os.getenv("HF_TOKEN")
```

## Why This Project Matters

This project demonstrates practical exposure to:

- AI-agent workflows
- tool-augmented LLM behavior
- Hugging Face model integration
- observability and tracing with Langfuse
- early-stage prototyping of intelligent assistants

## Possible Improvements

- convert the notebook into a Python package or app
- add a clean architecture diagram
- separate tools into reusable modules
- add prompt / trace screenshots
- define evaluation scenarios for agent quality
- add better error handling and result formatting

## Suggested Positioning

This repository is strongest when presented as an **AI agent prototype** or **LLM workflow experiment**, not as a production-ready system. Framing it honestly makes it more credible to recruiters.

## Author

**Jay Dhobale**
