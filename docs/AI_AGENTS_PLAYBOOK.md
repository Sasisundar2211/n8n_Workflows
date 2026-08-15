# AI Agents Playbook (n8n)

This guide helps you design reliable AI agents in n8n: goal‑driven, tool‑aware, and safe to operate in production.

## 1) Define the Job
- **Single sentence goal:** What should the agent accomplish?
- **Inputs:** Where does data come from (webhook, CRM, Slack, etc.)?
- **Outputs:** What must the agent deliver (message, spreadsheet, ticket)?

## 2) Pick the Right Agent Pattern
- **Router:** Classifies inputs then routes to specialized sub‑flows.
- **Planner → Executor:** LLM drafts steps; nodes execute tools.
- **ReAct / Tool‑Use:** LLM reasons, calls tools, then responds.
- **Human‑in‑the‑Loop:** Add approvals before critical actions.

## 3) Tooling & Integrations
- Keep tools **small and explicit** (one tool per action).
- Provide **structured inputs** (JSON fields, clear schema).
- Add **fallbacks** (retry, alternative provider, or alert).

## 4) Memory & Context
- **Short‑term memory:** Pass only relevant context per run.
- **Long‑term memory:** Store summaries in a database or vector store.
- **Privacy:** Never store secrets inside prompts.

## 5) Prompting Basics
- Use a **system prompt** with rules and constraints.
- Supply **examples** of ideal outputs.
- Ask for **structured output** (JSON or markdown).
- Keep prompts **short and consistent**.

## 6) Guardrails & Safety
- Add **input validation** nodes before LLM calls.
- Include **allow/deny lists** for tools and domains.
- Use **human approval** before emailing, posting, or purchasing.

## 7) Evaluation & Quality
- Log key fields (input, decision, output, tool calls).
- Create **test cases** with expected results.
- Review outputs weekly and adjust prompts.

## 8) Cost & Performance
- Use smaller models for classification/triage.
- Cache results where possible.
- Batch requests to reduce API overhead.

## 9) Production Readiness Checklist
- ✅ Credentials stored in n8n
- ✅ Error handling + notifications
- ✅ Retry policy
- ✅ Rate limit controls
- ✅ Audit log for actions

---

If you want a new AI agent template, open an issue with:
- The goal
- The tools it needs
- Example input/output
