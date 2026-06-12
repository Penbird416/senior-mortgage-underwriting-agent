# Senior Mortgage Underwriting Agent

A multi-agent AI system built with **LangGraph** that automates intelligent mortgage loan analysis. Specialized agents collaborate in a coordinated workflow to process applications end-to-end.

## What it does

- **PII Sanitization** — strips and redacts sensitive applicant data before processing
- **Bias Detection** — flags potential demographic bias in underwriting decisions
- **RAG Policy Compliance** — retrieves and applies lender policy documents via retrieval-augmented generation
- **Specialist Agent Workflow** — parallel agents evaluate income, credit, property, and risk independently
- **Human-in-the-Loop** — escalation paths route edge cases to human reviewers before final decision

## Architecture

```
Intake → PII Sanitizer → [Income Agent | Credit Agent | Property Agent | Risk Agent] → Aggregator → HITL Gate → Decision
```

Built on LangGraph's state machine architecture with typed state passing between nodes.

## Stack

- LangGraph
- OpenAI API
- Python 3.10+

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env
# Add your API keys to .env
jupyter notebook senior_mortgage_underwriting_agent.ipynb
```

## Environment variables

See `.env.example`.
