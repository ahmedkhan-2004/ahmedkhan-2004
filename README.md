<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/feedback-loop-dark.svg">
  <img alt="Ahmed Khan, Applied AI Engineer. Animated diagram of a feedback loop: market research becomes generation constraints, agents generate, independent review checks the output, a human approves before publishing, and outcome data feeds the next run." src="./assets/feedback-loop-light.svg" width="100%">
</picture>

[LinkedIn](https://www.linkedin.com/in/ahmedkhan04/) · [Email](mailto:ahmed2004.akn@gmail.com) · [Repositories](https://github.com/ahmedkhan-2004?tab=repositories)

</div>

I build the systems around AI models: the context they receive, the tools they can use, the checks their outputs must pass, and the feedback that improves the next run.

At **Printerpix**, I own a research-to-publishing agent system spanning **nine markets and five product lines**. The loop above is that system: market intelligence shapes what agents generate, independent review decides what survives, a human approves every external action, and outcome data feeds the next run.

## Selected engineering work

### Agent harness and release controls

Built on Claude Code with custom subagents and hooks, the harness separates generation, review, and tooling responsibilities. Structured outputs and stateful handoffs carry work between stages, and nothing reaches an external platform without human approval.

- **15 pre-release checks** covering citations, product fidelity, legibility, deduplication, and composition.
- Every send is bound to the exact asset, account, and platform, with approval expiry, dry-run/live separation, and duplicate prevention.
- Supervised publishing is isolated from unattended schedules.

### Evaluation that checks the evaluator

Review is split into independent product-accuracy, artwork-fidelity, and creative-quality passes. I then audited the automated checks themselves: a pixel-level review of **130 renders** exposed blind spots in rejection logic and recovered a strong candidate without another generation call. Failures become reusable production recipes.

Joining **127 published assets** to platform outcomes, I traced repetitive output to legacy briefs and stale assets, then added classification and batch-diversity checks. I also caught a platform reporting anomaly before it could steer creative decisions.

### Market intelligence that changes generation

Weekly competitor sweeps and scheduled trend checks turn observations into **source-linked findings and generation constraints**. Publication records join back to performance data, closing the loop from research to outcome. The findings drove a redesign of the cover-creative system.

### Model selection by evidence

I set up the office's **self-hosted Qwen infrastructure** and own its authenticated API integration and task-level routing, weighing quality, cost, and latency per task.

I tested **Jev through Vercel AI Gateway** against human-labelled examples, separate development and holdout sets, and rule-based baselines. The results gave it a focused role in occasion detection and relevance triage, while deterministic code beat it on caption mechanics and stayed in place. Next, I'm extending the same evaluation to Arabic-first open models (Jais 2, ALLaM) on Gulf-dialect tasks.

### Data applications and diagnostic agents

- **Audit automation:** a FastAPI/Next.js agent that inspects tags, triggers, event schemas, and consent states across **nine Google Tag Manager properties**, producing evidence-linked findings for human review.
- **Financial data:** co-built a BigQuery contribution-margin platform joining analytics, advertising, email, and product data, with source-parity checks and 476+ automated platform tests.

<details>
<summary><strong>Earlier work: retrieval, backend systems, and hardware</strong></summary>
<br>

- **Dasseti:** document Q&A prototypes with C#/.NET 8, Semantic Kernel, and PostgreSQL, covering chunking, retrieval, and plugin interfaces; evaluated MCP and agent architectures.
- **Karbon-Art:** Python/scikit-learn predictive-maintenance prototypes, and restored USB-serial telemetry ingestion from physical sensors.
- **NextGen Trader:** Kafka and PostgreSQL backend and reporting components for event-driven trading workflows.

</details>

## Engineering toolkit

| Area | Tools and practices |
| :--- | :--- |
| Agent systems | Claude Code harness (subagents, hooks), multi-agent orchestration, generator/reviewer separation, tool calling, structured outputs, stateful handoffs, human-in-the-loop approval, MCP, RAG |
| Evaluation | Evaluator audits, rubric-separated review, human-labelled datasets, dev/holdout splits, rule-based baselines, outcome-data joins, failure analysis, regression tests |
| Models | Self-hosted Qwen, Vercel AI Gateway, task-level routing, cost and latency trade-offs, Semantic Kernel |
| Languages | Python, TypeScript/JavaScript, SQL, C# |
| Backend and data | FastAPI, Next.js/React, Node.js, .NET 8, BigQuery, PostgreSQL, Kafka, Docker |
| Development | Claude Code as my primary environment, alongside Codex; every generated change is reviewed and tested before merge |

## How I work

**Trace the failure.** Inspect inputs, intermediate artifacts, tool behavior, and outputs before choosing a fix.

**Separate evidence from judgment.** Keep source facts, model assessments, deterministic checks, and human decisions distinguishable.

**Control side effects.** Generating a proposal and authorizing an external action are separate engineering responsibilities.

**Make improvements testable.** Turn a failure into a reproducible case, compare it against a baseline, and keep the check after the fix.

---

**BEng (Hons) Computer Systems Engineering, First Class Honours**, Middlesex University Dubai, 2025

Interested in applied AI and agent-engineering roles with ownership across implementation, evaluation, and deployment. Based in Dubai.
