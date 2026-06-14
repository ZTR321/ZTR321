# Hi, I'm Taoran Zhang / 张涛然

Master's student in Data Science at City University of Hong Kong.  
I am focusing on **AI Agent application development**, **LLM application engineering**, and **RAG-based research systems**.

My current goal is to build LLM applications that are not only runnable, but also controlled, traceable, evaluable, and practical for real business workflows.

## Current Focus

- AI Agent workflows with clear tool boundaries
- Browser Agent / computer-use tasks with human approval gates
- RAG systems with citations, no-answer behavior, and evaluation
- Agent memory for personalized research and decision support
- LLM application engineering with schema validation, trace, and fallback

## Featured AI Agent Projects

### 1. Enterprise Recruiting Browser Agent Workflow

A controlled browser-agent workflow for recruiting portals and other enterprise web workflows.

What it demonstrates:

- Browser observation with Playwright and browser-use
- Structured `JobPosting` schema extraction
- Rule-based and LLM-based extraction cross-checking
- Qwen-VL screenshot safety review
- Human-in-the-loop gates for risky actions such as apply, submit, login, or authorization
- Trace, dashboard, offline evaluation, and fallback handling

Verified local results:

- Unit tests: `25 passed`
- Mock workflow evaluation: `4 / 4`
- Multi-site detail-page evaluation: `6 / 6`
- Read-only real-page observation found 272 Bilibili campus positions and an LLM Agent related role

Core idea:

> Enterprise Agent systems should not let the model act without boundaries. The model should work inside a controlled, evaluable, traceable, and recoverable workflow.

### 2. Memory-Augmented AI Industry Research Agent

A research-style Agent for AI industry reports, combining RAG, long-term memory, evidence citations, and evaluation.

What it demonstrates:

- Plan -> retrieve -> verify -> report workflow
- Hybrid retrieval with keyword, concept, and local embedding-style scoring
- Evidence reranking and citation binding
- Long-term memory retrieval for personalized interview angles
- No-answer handling when evidence is insufficient
- Evidence-tension detection for conflicting or tradeoff-heavy topics
- Citation metrics and report evaluation

Verified local results:

- Unit tests: `7 passed`
- Generated AI Agent industry report with 6 sources, 5 insights, and 20 evidence snippets
- Citation precision: `1.0`
- Citation coverage: `1.0`
- Evaluation accuracy for memory recall, JD fit, and industry report: `1.0`

Core idea:

> A research Agent should not only generate fluent reports. It should prove where each conclusion comes from, expose uncertainty, and make the workflow reviewable.

## Earlier LLM Projects

### Qwen2.5-7B Local SFT Practice

- Resource-constrained local instruction fine-tuning practice
- Qwen2.5-7B, Unsloth, LoRA / QLoRA, 4-bit quantization
- Focus on dataset formatting, training configuration, and basic validation

### LangGraph Finance Workflow

- Researcher / Tool / Reviewer workflow
- LangGraph, Tool Calling, Gradio, prompt-based compliance review
- Focus on tool integration, workflow boundaries, and explainable system design

## Tech Stack

- **Languages:** Python
- **LLM Apps:** LangChain, LangGraph, browser-use, Playwright, Qwen, Qwen-VL, DeepSeek API
- **RAG / Research:** hybrid retrieval, rerank, citation, no-answer, evidence tension, evaluation
- **Training Basics:** PyTorch, Hugging Face, Unsloth, LoRA / QLoRA, SFT
- **Engineering:** Pydantic, Typer, pytest, HTTP/Requests, HTML parsing, Git

## What I Am Looking For

Internship roles in:

- AI Agent application development
- LLM application engineering
- RAG / Agent workflow engineering
- AI Coding / Agent evaluation / enterprise AI tools

Preferred location: Shanghai.  
Availability: can start within one week, 5 days per week.

## Contact

- Email: `19105651915@163.com`
- GitHub: [github.com/ZTR321](https://github.com/ZTR321)

---

I keep my projects interview-explainable: what problem they solve, how the workflow is designed, how the system is evaluated, and where the current boundaries are.
