# Taoran Zhang / 张涛然

Master's student in Data Science at City University of Hong Kong.  
I focus on **AI Agent application development**, **LLM application engineering**, and **RAG systems for real business workflows**.

I am currently building Agent projects around one principle:

> Put the model inside a controlled workflow: clear schema, tool boundaries, trace, evaluation, fallback, and human approval for high-risk actions.

## Featured Projects

| Project | What It Solves | Core Stack | Verified Results |
| --- | --- | --- | --- |
| **Enterprise Web Workflow Automation Agent**<br>企业网页流程自动化 Agent 系统 | Turns messy enterprise web pages into a controlled Agent workflow for reading pages, extracting business objects, drafting form fields, and blocking risky actions before submit. Recruiting portals are the demo scenario; the same pattern can transfer to OA, CRM, supplier portals, and internal dashboards. | Python, Playwright, browser-use, Qwen, Qwen-VL, Pydantic, pytest, action policy, dry-run form filling | `28 passed`; 5-portal offline benchmark `5/5`; dry-run form plan blocks upload/submit; real read-only Bilibili observation found 272 positions |
| **LangGraph Memory-Augmented Industry Research Agent**<br>基于 LangGraph 的长期记忆型行业研究 Agent 系统 | Generates AI industry research reports with evidence, citations, memory recall, retry, and human-review checkpoints instead of unsupported fluent summaries. | Python, LangGraph, RAG, local memory, hybrid retrieval, optional DashScope/Bailian embedding and rerank, citation evaluation, pytest | `12 passed`; AI Agent industry report with 6 sources, 5 insights, 20 evidence snippets; citation precision `1.0`; citation coverage `1.0` |

## Project 1: Enterprise Web Workflow Automation Agent

A browser Agent prototype for enterprise web workflows. It is not a script that blindly clicks buttons. It observes web pages, extracts structured information, classifies action risk, drafts form fields in dry-run mode, and requires human confirmation before any high-risk operation.

**Why I built it**

Enterprise processes still happen inside web pages: application forms, approval pages, supplier portals, CRM pages, and internal dashboards. A useful Agent must handle unstructured pages, dynamic UI, risky buttons, and failure recovery.

**What I implemented**

- Read-only browser observation with Playwright and browser-use.
- Structured schemas: `JobPosting`, `FormFillPlan`, `ActionPolicyDecision`, `WorkflowTrace`.
- Rule extraction and Qwen text extraction cross-checking.
- Qwen-VL screenshot safety review for visible risky actions.
- Action policy engine for `read_only`, `fill_draft`, `upload_file`, `submit`, `authorization`, `payment`, and `destructive`.
- Application form dry-run filling with field confidence and manual-review flags.
- Trace files, dashboard reports, deterministic tests, and multi-portal offline benchmark.

**What this proves**

- I can design Agent systems with controlled tool boundaries instead of one-off demos.
- I understand why real-world Agent workflows need schema validation, audit trails, risk gates, and fallback paths.
- The browser workflow is transferable beyond recruiting portals to enterprise operations.

## Project 2: LangGraph Memory-Augmented Industry Research Agent

A research Agent for AI industry reports. It reads a source pack, retrieves evidence, recalls long-term memory, verifies citation quality, retries when evidence is weak, and enters human review when there is evidence tension.

**Why I built it**

Research Agent outputs often look complete but lack source grounding. I wanted the system to show where each conclusion comes from, when evidence is insufficient, and how the workflow reached the final report.

**What I implemented**

- LangGraph `StateGraph`: `plan -> retrieve_sources -> retrieve_memory -> retrieve_evidence -> verify -> retry / human_review -> report`.
- Local long-term memory for profile, project background, and interview angles.
- Hybrid retrieval with keyword, concept, and local embedding-style scoring.
- Optional DashScope/Bailian embedding and rerank API path with local fallback.
- Citation binding, no-answer handling, evidence-tension detection, and report evaluation.
- Checkpoint interrupt/resume demo for human review.
- Evaluation for memory recall, theme coverage, expected source recall, citation precision, and citation coverage.

**What this proves**

- I can build stateful Agent workflows rather than simple RAG Q&A.
- I can separate retrieval, verification, retry, review, and report generation into testable nodes.
- I care about evidence quality, traceability, and hallucination control.

## Engineering Focus

- **Agent workflow:** tool calling, state schema, conditional routing, retry loop, human-in-the-loop, trace.
- **Browser / computer-use:** Playwright, browser-use, read-only observation, action safety policy, dry-run form filling.
- **RAG / research:** source parsing, hybrid retrieval, rerank, citation, no-answer, evidence tension.
- **LLM integration:** Qwen, Qwen-VL, DeepSeek-compatible APIs, structured JSON output, fallback handling.
- **Model adaptation background:** PyTorch, Hugging Face, Qwen2.5-7B instruction tuning, LoRA / QLoRA, chat template.
- **Python engineering:** Pydantic, Typer, pytest, HTTP/Requests, HTML parsing, Git.

## Earlier Background Projects

- **Qwen2.5-7B Local SFT Practice:** local instruction tuning workflow with Unsloth, LoRA / QLoRA, 4-bit quantization, dataset formatting, and basic validation.
- **LangGraph Finance Workflow:** Researcher / Tool / Reviewer workflow with tool calling, market-data API wrapper, parameter validation, timeout handling, and review logic.

## Target Roles

I am looking for internships in:

- AI Agent application development
- LLM application engineering
- RAG / Agent workflow engineering
- AI Coding Agent / Agent evaluation / enterprise AI tools

Preferred location: Shanghai.  
Availability: can start within one week, 5 days per week.

## Contact

- Email: `19105651915@163.com`
- GitHub: [github.com/ZTR321](https://github.com/ZTR321)

---

I keep my projects interview-explainable: what problem they solve, how the workflow is designed, how the system is evaluated, and where the current boundaries are.
