<a href="https://ibrahimsaleem.com">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:4F46E5,50:7C3AED,100:06B6D4&height=180&section=header&text=Project%20%26%20Repository%20Index&fontSize=34&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full%20catalogue%20of%20every%20public%20repo%20—%20categorised%2C%20with%20context&descSize=15&descAlignY=60" alt="header" />
</a>

> Complete record of every public repository on [github.com/ibrahimsaleem](https://github.com/ibrahimsaleem) — **62 repos** grouped by theme, plus the **2 founder ventures** (HireEase / AplyEase, WarmNode) whose core code is private. Each entry: what it is, the stack, and where it stands.
> Generated **August 2026**. Star counts and dates are point-in-time snapshots.
> Back to the [profile README](./README.md).

---

## 📇 Contents

| # | Category | Repos |
|---|---|---|
| 0 | [Founder Ventures](#0-founder-ventures) | 2 ventures |
| 1 | [AI Security, Red Teaming & Pentest Automation](#1-ai-security-red-teaming--pentest-automation) | 12 |
| 2 | [MCP Servers & Structured Reasoning](#2-mcp-servers--structured-reasoning) | 3 (+1 cross-listed) |
| 3 | [AI Agent Harnesses, Platforms & Observability](#3-ai-agent-harnesses-platforms--observability) | 5 |
| 4 | [LLM Cost Optimization & Routing](#4-llm-cost-optimization--routing) | 3 |
| 5 | [RAG & Semantic Search](#5-rag--semantic-search) | 2 |
| 6 | [GenAI Applications & Career Tools](#6-genai-applications--career-tools) | 5 |
| 7 | [Full-Stack Web Apps & SaaS](#7-full-stack-web-apps--saas) | 11 |
| 8 | [Cybersecurity Education & Community](#8-cybersecurity-education--community) | 5 |
| 9 | [ML & Network Security Coursework / Research](#9-ml--network-security-coursework--research) | 3 |
| 10 | [Portfolio, Résumé & Personal Sites](#10-portfolio-résumé--personal-sites) | 5 |
| 11 | [Early Projects (2022, bootcamp / learning)](#11-early-projects-2022-bootcamp--learning) | 4 |
| 12 | [Forks](#12-forks) | 2 |

**Legend** — ★ stars · 🍴 fork · 📦 archived/paused · 🌐 has live deployment · 📄 linked to a paper

---

## 0. Founder Ventures

AI products founded and built end-to-end — product strategy, AI architecture, full-stack delivery, and security. Core application code is private; public sub-repos are noted per venture.

### HireEase / AplyEase — Founder & AI Product Engineer · *Nov 2024 – Present*
**[hireease.me](https://hireease.me) · [aplyease.com](https://aplyease.com)** — AI-powered "done-for-you" job-application platform.
- Automated résumé tailoring + ATS optimization + job matching, plus trained human specialists who apply on the client's behalf; clients see every submission (job, company, status, résumé used, recruiter-mail flag) in a real-time dashboard.
- **Traction: 40,000+ job applications processed for 300+ clients. Applied to Y Combinator.**
- **Stack:** full-stack TypeScript monorepo — React 18 / Vite / Tailwind / Radix UI / shadcn / TanStack Query / Wouter · Express + Drizzle ORM / PostgreSQL · Passport.js session auth + JWT + bcrypt · Zod / drizzle-zod shared validation.
- **Built:** the AI résumé-tailoring engine, a LaTeX→PDF compilation pipeline, and a three-role (Client / Employee / Admin) operations portal with an Applied→Screening→Interview→Offer/Rejected/Hired lifecycle.
- **Public sub-repos:** [`aplyease-backend`](https://github.com/ibrahimsaleem/aplyease-backend) · [`aplyease-frontend`](https://github.com/ibrahimsaleem/aplyease-frontend) · [`aplyeasedash`](https://github.com/ibrahimsaleem/aplyeasedash) · [`hireeaseemployee`](https://github.com/ibrahimsaleem/hireeaseemployee) (standalone employee portal — single Express service serving the React SPA + JWT API on shared Supabase PostgreSQL, with the AI résumé-tailoring endpoint and LaTeX→PDF compile).

### WarmNode (WarmNodeAI) — Founder & AI Engineer · *Apr 2026 – Present*
**[warmnode.me](https://warmnode.me)** — privacy-focused AI relationship assistant: find who in your network can help, why they matter, and what message to send.
- **Solo founder · YC Fall 2026 application submitted · pre-seed, no funding taken.**
- **Stack:** mobile-first PWA — React / TypeScript / Vite · Node / Express / TypeScript · PostgreSQL (Supabase) / Drizzle ORM with programmatic RLS policies · custom secure JWT auth (no third-party provider).
- **AI:** Google Gemini (`gemini-1.5-flash`) for semantic contact categorization and natural-language network queries, with a graceful local-keyword-search fallback when no key is present.
- **Shipped:** CSV contact import, QR public profiles, and Apple Wallet pass (`.pkpass`) generation for privacy-conscious profile sharing at events. Roadmap: Google Wallet, native contact sync, relationship-graph visualization, Stripe premium quotas.

> `warmnode` (application code) and `warmnode-fundraising` (YC / investor materials) are private repos and are not part of the public catalogue below.

---

## 1. AI Security, Red Teaming & Pentest Automation

The core of the portfolio: turning LLMs and agents into security instruments, and securing the agent stack itself.

### [PentestThinkingMCP](https://github.com/ibrahimsaleem/PentestThinkingMCP) — ★38 · 🍴7 · 📄
**Systematic, AI-powered penetration-testing reasoning engine delivered as an MCP server.** · JavaScript · Created May 2025 · Last active Aug 2025
- Guides an LLM through attack-path planning, CTF/HTB solving, and automated pentest workflows using **Beam Search** and **Monte Carlo Tree Search**, with attack-step scoring and per-step tool recommendations.
- Integrates Metasploit, Nmap, and Burp Suite; secured with prompt-injection defenses, I/O validation, and rate limiting per OWASP Agentic AI Threat Modeling.
- Benchmark: compromised HTB "Lame" in ~3 min (~$0.03/run); 90% accuracy across 50+ scenarios. Basis of the **IEEE FMLDS 2025** LIMA paper.
- **In production:** ~10,000 monthly tool calls at **99.99% reliability** on [Smithery](https://smithery.ai/server/@ibrahimsaleem/pentestthinkingmcp), integrated across Claude, Cursor, and VS Code — among the most-used pentesting MCP servers on the platform.

### [ClawProtect](https://github.com/ibrahimsaleem/ClawProtect) — ★1 · 📄 [architecture paper](https://github.com/ibrahimsaleem/ClawProtect/blob/main/ClawProtect%20A%20Defense-in-Depth%20Security%20Stack%20for%20AI%20Agent%20Gateways.pdf)
**Defense-in-depth AI security stack for agent gateways.** · Go 1.24+ / Python 3.11+ · Created Mar 2026
- **Content-aware HTTP security proxy** + YAML policy engine — detects prompt injection, PII, secrets, and vulnerability patterns in real-time LLM inputs/outputs.
- Adds a **kernel-level eBPF syscall monitor** and a network-egress firewall to isolate containerized agent workloads, all **unified by a cross-layer event bus** for adaptive response across app / network / kernel layers — 29 modules.
- Ships a policy language, structured audit-log format, Prometheus-compatible metrics, install guide, WSL2 notes, and an academic-style architecture paper.

### [mcp-security-lab](https://github.com/ibrahimsaleem/mcp-security-lab)
**Runnable MCP setup with seven deliberate vulnerabilities and their fixes.** · HTML / Python (FastMCP, Uvicorn) · Created Aug 2026
- Built against the current official MCP spec (`2026-07-28`) and the **OWASP MCP Top 10**; every risk is a working exploit script paired with a fixed server.
- Web dashboard streams live exploit output over WebSockets; includes a field reference for all ten OWASP MCP categories and a before/after analysis of the spec's stateless rewrite.
- Fully local — nothing touches real systems.

### [PenTestAgent](https://github.com/ibrahimsaleem/PenTestAgent) — ★2 · 📄
**PentestingAgentUsingOmniTool — automated security scanning and execution framework.** · Python · Created May 2025 · Last active Jun 2025
- Extension of OmniTool that chains **Nmap**, **RustScan**, and **Google Gemini**: takes a target, scans, analyzes results, and executes actionable steps iteratively in a closed feedback loop until the user stops.
- References the OmniTool arXiv paper (2408.00203).

### [Pen-AI-deployed](https://github.com/ibrahimsaleem/Pen-AI-deployed) — ★2 · 🌐
**AI-powered pentesting tool that scans Python projects for vulnerabilities.** · Python (Flask) · Created Feb 2025 · Last active Apr 2025
- Integrates **Bandit** for static scanning, **Gemini** for remote analysis, and **Ollama/LLaMA** for local analysis; prioritized findings with remediation guidance.
- Runtime-supplied API keys (no hardcoded secrets); real-time SSE / conversational web UI.

### [local-pentest-rag-mcp](https://github.com/ibrahimsaleem/local-pentest-rag-mcp) — ★2
**"HTB Solver" — simplified HackTheBox solver using web search, RAG, and MCP.** · Python · Created May 2025 · Last active Jun 2025
- Step-by-step guidance issuing exactly one command at a time, output analysis, session/flag tracking, and local document retrieval for machine walkthroughs.

### [LocalPentestAgent](https://github.com/ibrahimsaleem/LocalPentestAgent) — ★1
**Local RAG-based pentesting agent for HackTheBox machines.** · Python · Created May 2025
- Multiple interaction modes and built-in token tracking; offline-first design.

### [PentestAgentMCP](https://github.com/ibrahimsaleem/PentestAgentMCP) — ★2 · 🍴1
**Scaffold for building an automatic pentesting agent from MCP servers.** · Created May 2025
- Early exploration that fed into PentestThinkingMCP and the LIMA research line.

### [Evil-Trace](https://github.com/ibrahimsaleem/Evil-Trace)
**EvilTrace AI — autonomous DFIR incident-response agent.** · TypeScript · Created Jun 2026
- "FIND EVIL" Devpost hackathon submission. Multi-agent pipeline: Collector → Tool Runner → Hypothesis → Verification → Self-Correction → IOC Enrichment → Report.
- **Zero-hallucination gate**: rejects any LLM-asserted hypothesis (credential dumping, exfiltration, …) unless exact artifact evidence is verified in Sysmon / Zeek / Auth logs.
- Optional Exa Search IOC enrichment (informational only); offline mock mode; Streamlit dashboard; judge-ready forensic reports with full audit trails.

### [network-exposure-reporter](https://github.com/ibrahimsaleem/network-exposure-reporter)
**Security-posture reporting tool: IP / CIDR / ASN → analyst-reviewable exposure report.** · Python · Created Jul 2026
- Produces a Word `.docx` draft + Excel `.xlsx` companion + Matplotlib charts + AI narrative, grounded in real passive vulnerability data.
- Architectural principle: **deterministic code does all counting, scoring, and classification; the LLM only writes prose and proposes taxonomy candidates.** Every number is verified against computed statistics.
- FastAPI single-page UI; mock mode runs with zero network calls.

### [mdscanner](https://github.com/ibrahimsaleem/mdscanner)
**Scans Markdown for security and integrity risks before it is rendered, fed to an AI agent, or committed to docs.** · Python · Created Feb 2026
- Curated regex rules for code execution / injection (`<script>`, `onerror=`, `javascript:` links), **prompt injection** ("ignore previous instructions", DAN-style persona reassignment, hidden HTML-comment instructions), obfuscation (`eval(atob())`, zero-width Unicode), and credential exposure (AKIA keys, private-key blocks).
- Aimed at README files, SKILL files, and docs-as-code pipelines.

### [openclawscanner](https://github.com/ibrahimsaleem/openclawscanner) — ★1
**Cross-platform detection scripts for the "OpenClaw" agent (and its former names Moltbot / Clawdbot).** · Shell / PowerShell · Created Feb 2026
- `detect-openclaw.sh` (macOS/Linux) and `detect-openclaw.ps1` (Windows) with machine-readable output and opinionated exit codes for MDM/RMM wiring (Intune, Jamf, Kandji, …).
- Optionally scans installed skills against a maintained list of **341 known-malicious skills** (`risk.txt`).

---

## 2. MCP Servers & Structured Reasoning

Reusing the "ThinkingMCP" architecture (Beam Search + MCTS guiding an LLM step-by-step) across new domains.

### [EncoderThinking](https://github.com/ibrahimsaleem/EncoderThinking) — ★1 · 📄
**EncoderThinkingMCP — MCP server that makes an LLM "think like an ML engineer" for encoder-decoder development.** · JavaScript · Created Oct 2025
- Automated training-path planning via Beam Search / MCTS, step scoring and prioritization, per-step tool recommendations (PyTorch, TensorFlow, Keras, scikit-learn), and framework-specific code generation.
- Direct adaptation of the PentestThinkingMCP architecture. Subject of the **IEEE Southwest 2026** paper (with T. Banerjee).

### [Swaggermcp](https://github.com/ibrahimsaleem/Swaggermcp) — ★2
**SwaggerMCP — turns Python functions into REST API endpoints with full Swagger docs, driven by MCP.** · Python (FastAPI) · Created Jul 2025
- AST-based code parsing → FastAPI generation → live testing, hot reload, Docker-ready.
- Full MCP support so Claude / Cursor can create and manage APIs directly.

### [PentestThinkingMCP](https://github.com/ibrahimsaleem/PentestThinkingMCP)
The original of the family — see [category 1](#1-ai-security-red-teaming--pentest-automation) for full details.

### [github-controller](https://github.com/ibrahimsaleem/github-controller) — ★1
**Programmatic GitHub control surface for agents.** · Created May 2025 · minimal / experimental
- Early utility for letting an agent drive GitHub operations; superseded by the GitHub integration inside `claude-portal`.

---

## 3. AI Agent Harnesses, Platforms & Observability

Building, branding, and instrumenting agent runtimes — and putting guardrails around them.

### [compass](https://github.com/ibrahimsaleem/compass) — *contributor, not primary author*
**Team-built multiplayer agent platform for work — Slack + web — with the Ward guardrail layer.** · TypeScript (Fastify, Postgres, Slack Bolt, Vite + Lit) · Created Aug 2026
- Every employee and every room gets its own isolated, scoped workspace: memory, files, keychain view, permissions, crons, web apps, durable sandbox.
- **Ward guardrail boundary**: screens external data and tool results before the model, enforces command policy, and gates actions behind human approval — three postures (Strict / Auto / Dangerous).
- Vendor-neutral: Pi, OpenCode, Codex, and Claude Code all drive the same core; `compass` CLI deploys to Fly or AWS.
- *Contribution scope: guardrail / security side. Majority of the codebase is other contributors' work — listed here for completeness, not as a solo project.*

### [saleem-coding-agent](https://github.com/ibrahimsaleem/saleem-coding-agent) &nbsp;— *canonical repo*
**"Saleem Harness" — an actively-developed personal coding-agent CLI (`saleem`).** · TypeScript (pnpm workspace, Cordis) · Created Aug 2026
- Fully **plugin-based on the [Cordis](https://github.com/cordiverse/cordis) composability framework**; installable alongside existing agent-harness setups without replacing them.
- **Default-on, preventive tool-call safety guard** (`tool-guard-saleem`) that intercepts and blocks unsafe tool executions *before* they run — not logging or alerting after the fact.
- Local Web UI (`127.0.0.1:3080`) + CLI entrypoint with hot-reloadable plugins. Developer preview.
- `saleem-harness` / `saleem-harness-cli` are earlier siblings that shared this codebase; **`saleem-coding-agent` is the one to reference.**

### [dsh-dashboard](https://github.com/ibrahimsaleem/dsh-dashboard)
**"DSH Monitor" — local real-time observability dashboard for DeepSeek Harness (`dsh`).** · JavaScript (Node.js, Express) · Created Aug 2026
- Aggregate token usage, cost, live agent activity, tool calls, permission/sandbox risk, and a reactive kill switch — all on one page.
- **Entirely external**: no plugin, no fork, no changes to the harness. Reads the same session logs `dsh` already writes to disk.

### [claude-portal](https://github.com/ibrahimsaleem/claude-portal)
**Control Claude Code from your phone.** · Python (FastAPI + WebSocket) · Created Jun 2026
- Mobile-optimized chat UI, real-time activity feed (reads/commands/searches/edits), streaming responses, filesystem browser, GitHub integration (repos/clone/pull/commit/push), system monitor, permission gating for destructive ops, file upload, persistent sessions, ngrok tunneling.

### [ai-job-search](https://github.com/ibrahimsaleem/ai-job-search) — 🍴
**AI job-application framework built on Claude Code.** · Fork · Created Jul 2026
- "The job search that runs on your machine" — evaluate postings, tailor CVs, write cover letters, prep interviews. Forked to adapt and own.

---

## 4. LLM Cost Optimization & Routing

Proving cost-per-resolved-task savings with real dollars, not vendor benchmark numbers — an AI-Engineer JD pattern.

### [switchlane](https://github.com/ibrahimsaleem/switchlane) · [demo video](https://www.linkedin.com/posts/ibrahimsaleem91_aiengineering-llm-tokenoptimization-activity-7496113235692105728--8Eg)
**SwitchLane — cost-aware LLM request routing platform.** · Python · FastAPI · vanilla JS · Created Aug 2026
- A trained classifier embeds each incoming prompt and scores whether the expensive model would meaningfully beat a lightweight one, then routes to **exactly one model per request (no dual-calling)** — routing decision ~**1 ms**.
- Full-stack site: live chat interface with real-time per-message latency/token tracking, a **Model Advisor** for cost-benefit analysis, and a methodology/architecture page.
- **Benchmarked** across 3 configs on the same **1,500 prompts** with real token usage and real API pricing: **40.5% cost reduction at 100% task pass rate**; **74.6% cost savings** in a separate live chat session.
- Routing engine: **RouteLLM** (Apache-2.0, UC Berkeley/LMSYS + Anyscale), vendored in full with attribution.

### [llm-cost-aware-routing](https://github.com/ibrahimsaleem/llm-cost-aware-routing)
**Local, budget-bounded validation of cost-aware routing against real strong/weak models.** · Python · Created Aug 2026
- Measures real cost-per-resolved-task vs. an always-expensive baseline with **actual token usage and actual dollar costs**.
- The research/validation counterpart to SwitchLane; includes a full background context doc for an internal proposal.

### [TokenLess](https://github.com/ibrahimsaleem/TokenLess) — ★1
**Token-optimization hub for teams building AI apps.** · Python 3.9+ · Created May 2026 · Last active Jun 2026
- Structured docs, employee training paths with schedule/levels, developer guidelines, and system-prompt templates.
- Packages reusable **AI skill packs** — token & cost tracking, context optimization, enterprise efficiency guidelines — that **plug directly into Claude Code, Windsurf, MCP agents, and Copilot** workflows.
- **TokenWatch** — a zero-dependency Python library for local LLM cost tracking and budget alerts. LiteLLM gateway demo with guardrails and prompt compression.

---

## 5. RAG & Semantic Search

### [ultrasearch](https://github.com/ibrahimsaleem/ultrasearch) — ★1
**UltraSearch — lightning-fast laptop-wide RAG search built on LEANN.** · Python (Streamlit, Sentence Transformers, FAISS/HNSW) · Created Sep 2025
- Bundles **LEANN** (Low-Storage Vector Index): graph-based selective recomputation for ~97% less storage than conventional vector DBs, AST-aware code chunking, real-time indexing.
- Ollama / Gemini for generation.

### [LocalRAGAgent](https://github.com/ibrahimsaleem/LocalRAGAgent) — ★1
**Offline, privacy-preserving RAG system.** · Python · Created May 2025
- Converts PDF or plain-text files into a vector database, then answers queries against that context using a **local LLM via Ollama** — nothing leaves the machine.

---

## 6. GenAI Applications & Career Tools

### [AI-ResumeMaker](https://github.com/ibrahimsaleem/AI-ResumeMaker) — ★2 · 🌐
**Transforms a plain-text résumé into a professionally formatted LaTeX document.** · Python · Created Feb 2025 · Last active Jul 2025 · [live](https://airesumemaker.onrender.com/)
- Google Gemini analyzes, optimizes, and tailors the résumé to a target job description for ATS-friendliness; skills analysis + feedback; download/copy LaTeX for Overleaf. Passcode-protected login.

### [AI-ResumeMaker-Streamlit](https://github.com/ibrahimsaleem/AI-ResumeMaker-Streamlit) — ★3
**Streamlit build of the AI résumé generator.** · Python · Created Sep 2025
- Same engine as AI-ResumeMaker with a Streamlit UI: ATS optimization, file-upload support, Resume-Worded feedback integration.

### [AIResume](https://github.com/ibrahimsaleem/AIResume) — ★1
**Flask résumé maker with automated skills analysis and formatting.** · Python (Procfile / deploy-ready) · Created May 2025
- The earliest of the three résumé tools.

### [CareerPathAgent](https://github.com/ibrahimsaleem/CareerPathAgent) — ★2
**AI certification-roadmap agent and interactive tutor.** · Python (Flask + Google Gemini) · Created Aug 2025
- Two cooperating agents — a **Roadmap Agent** (personalized learning paths for Cybersecurity / Data Science / AI Engineering from a user profile) and a **Tutor Agent** (on-demand explanations).
- Interactive SVG roadmap with click-to-explain.

### [joblance](https://github.com/ibrahimsaleem/joblance)
**Job / freelance workflow experiment.** · Created Nov 2025 · minimal
- Early-stage; not yet documented.

---

## 7. Full-Stack Web Apps & SaaS

### HireEase / AplyEase — public components of the founder venture
> Full venture writeup and traction (40,000+ applications, 300+ clients, YC) in **[§0 Founder Ventures](#0-founder-ventures)**. These are the public repos split out of the private monorepo:
- **[aplyease-backend](https://github.com/ibrahimsaleem/aplyease-backend)** — ★2 · Express + TypeScript + Drizzle ORM API. Created Aug 2025.
- **[aplyease-frontend](https://github.com/ibrahimsaleem/aplyease-frontend)** — ★2 · React + Vite client. Created Aug 2025.
- **[aplyeasedash](https://github.com/ibrahimsaleem/aplyeasedash)** — ★1 · Python analytics/admin dashboard. Created Apr 2025.
- **[hireeaseemployee](https://github.com/ibrahimsaleem/hireeaseemployee)** — ★1 · "Aplyease Employee Portal": one Express service serving both the React (Vite + Tailwind) SPA and a JWT-auth API on shared Supabase PostgreSQL, with an AI résumé-tailoring endpoint and LaTeX→PDF compilation. Created Mar 2026.

### [Invoice-Management](https://github.com/ibrahimsaleem/Invoice-Management)
**"Power Clean Pro — Business Manager" for pressure-washing businesses.** · TypeScript · Created May 2026 · Last active Jun 2026
- pnpm-workspace monorepo: React + Vite + Tailwind + shadcn/ui + wouter + TanStack Query · Express 5 (esbuild) · PostgreSQL (Supabase) + Drizzle · **OpenAPI spec as source of truth** with Orval-generated React Query hooks + Zod schemas.
- Customers, invoices/quotations, payment tracking, outstanding-balance monitoring, PDF export via print CSS. Server-side total calculation to prevent sync mismatches.

### [ServiceDeskCRM](https://github.com/ibrahimsaleem/ServiceDeskCRM) — ★2
**Full-stack service-desk and ticket-management platform.** · ASP.NET Core 3.1 + Angular · Created Jul 2025
- Ticket creation/assignment/closure, automatic ticket-ID generation, bookmarking, change-approval workflow, resolution tracking, dashboard.
- Load-tested to 500 requests/second.

### [GroceryStoreAPI](https://github.com/ibrahimsaleem/GroceryStoreAPI) — ★2
**Full-stack grocery-store management application.** · ASP.NET Core + Entity Framework Core · Created Mar 2024 · Last active Jul 2025
- User authentication, product management, shopping cart, order processing, reviews. Layered architecture (Data Access / DTO / Interfaces / Models).

### [EcoShiftConnect](https://github.com/ibrahimsaleem/EcoShiftConnect) — ★1
**Eco-friendly load-shifting web app that helps households cut cost and carbon.** · TypeScript · Created Sep 2025
- Recommends optimal appliance-scheduling windows from real-time Houston-market electricity pricing and color-coded eco time bands (GREEN/BLUE/ORANGE/RED), with a gamified EcoPoints/rewards system and CO₂-reduction tracking.
- **Stack:** React 18 + Tailwind + Radix UI + Framer Motion + Recharts · Express + Drizzle ORM · Google Gemini for natural-language scheduling recommendations · optional OpenWeather integration.

### [InstaUnfollow](https://github.com/ibrahimsaleem/InstaUnfollow) — ★3
**Instagram Unfollower Manager.** · Created Jun 2023 · Last active Mar 2026
- Search users, view results, whitelist/non-whitelist management, bulk unfollow, and unfollowing logs — a user-friendly interface over unfollower tracking.

### [voiceease](https://github.com/ibrahimsaleem/voiceease)
**"VoiceEase" — marketing / lead-generation site around a voice-agent product.** · TypeScript · Created Dec 2025
- React + Vite (Radix UI, Tailwind, Framer Motion) over Express + Drizzle ORM / PostgreSQL with Passport session auth: account register/login, an "agent request" intake flow, demo-request and contact forms, and an admin dashboard (users, requests, leads, contacts, stats).
- The repo is the lead-capture shell; the underlying voice-agent functionality is not documented in-repo.

### [Asyncwebsite](https://github.com/ibrahimsaleem/Asyncwebsite)
**Async web app experiment.** · TypeScript · Created Jun 2026 · minimal / early-stage

---

## 8. Cybersecurity Education & Community

### [cstools](https://github.com/ibrahimsaleem/cstools) — ★6 · 🌐
**"CS Tool" — a complete cybersecurity website guide plus a toolbox of hands-on utilities.** · HTML/Python · Created Oct 2022 · Last active May 2025 · [sctool.web.app](https://sctool.web.app/)
- Explains common cyber threats and prevention, and ships working tools: Keylogger, text encryption/decryption (Caesar, Vigenère, Morse), MAC-address changer, reverse-shell demo, image steganography, and a risk calculator.
- The portfolio's most-starred education project.

### [WICYS-website-code](https://github.com/ibrahimsaleem/WICYS-website-code) — ★2
**Website for the Women in CyberSecurity (WiCyS) University of Houston chapter.** · React 19 + Vite 7 + Tailwind 4 + Framer Motion · Created Aug 2025
- Member authentication for protected resources, AI-powered career-development tools (external services on Render), Firebase hosting, SEO-optimized, mobile-first.

### [cybersecurity-roadmap](https://github.com/ibrahimsaleem/cybersecurity-roadmap) — ★1
**A learning-roadmap page for cybersecurity.** · HTML · Created Apr 2025 · minimal

### [Search-in-quran](https://github.com/ibrahimsaleem/Search-in-quran) — ★2
**Python regex project to search for any word in the Quran.** · Python · Created Sep 2022 · Last active May 2025

### [50-Interview-questions](https://github.com/ibrahimsaleem/50-Interview-questions) — ★2
**Curated set of 50 interview questions (with Python examples).** · Python · Created Sep 2022 · Last active Jul 2025

---

## 9. ML & Network Security Coursework / Research

### [ML-DDOS-Detection-Project](https://github.com/ibrahimsaleem/ML-DDOS-Detection-Project) — ★2
**Machine-learning pipeline for detecting DDoS attacks in network traffic.** · Created Mar 2025
- Group project ("Team Olympians") for the UH **Data Science for Cybersecurity** course.
- EDA → cleaning/preprocessing → feature engineering → SMOTE for class imbalance → train/tune/evaluate multiple models; proposes deep-learning follow-ups.

### [DDoS-Detection-and-Mitigation-Framework-Using-Software-Defined-Networking-SDN-](https://github.com/ibrahimsaleem/DDoS-Detection-and-Mitigation-Framework-Using-Software-Defined-Networking-SDN-) — ★2
**Real-time DDoS detection and mitigation using SDN's centralized control + ML.** · Created Feb 2025
- Traffic analysis, feature extraction, and dynamic threat mitigation with **Mininet**, **Ryu controller**, and **KNN**.

### [Face-Recognition-Attendance-Software](https://github.com/ibrahimsaleem/Face-Recognition-Attendance-Software) — ★2
**Face-recognition attendance system.** · Python · Created Feb 2022
- OpenCV **LBPH** recognizer + Haar-cascade face detection, Tkinter UI, SQL database for student records, CSV/Excel attendance export with timestamps.

---

## 10. Portfolio, Résumé & Personal Sites

### [ibrahimsaleem](https://github.com/ibrahimsaleem/ibrahimsaleem) — ★4
**GitHub profile README repo** — this repository. Contains the profile [`README.md`](./README.md), this project index, and the contribution-snake GitHub Action.

### [portfolio-project-updated](https://github.com/ibrahimsaleem/portfolio-project-updated) — ★2 · 🌐
**Current personal portfolio site.** · React / HTML · Created Aug 2025 · Last active Jul 2026 · [ibrahimsaleem-portfolio.web.app](https://ibrahimsaleem-portfolio.web.app)
- Cyber/AI-security design system: canvas MatrixRain background, glitch hero tagline, experience, research publications, projects, technical blog, certifications, and an AI chat assistant that answers questions about Ibrahim in real time.

### [portfolio-ib](https://github.com/ibrahimsaleem/portfolio-ib) — ★2 · Created Oct 2024 · earlier portfolio iteration.
### [portfolio](https://github.com/ibrahimsaleem/portfolio) — ★2 · Created Feb 2022 · first portfolio.
### [resume](https://github.com/ibrahimsaleem/resume) — ★2 · Created Feb 2022 · Last active Mar 2025 · hosted résumé.

---

## 11. Early Projects (2022, bootcamp / learning)

Front-end and ML fundamentals from LetsGrowMore / early self-study — kept for history.

| Repo | What it is | Stack | Created |
|---|---|---|---|
| [whatnext](https://github.com/ibrahimsaleem/whatnext) ★2 🍴1 🌐 | ML movie-recommendation web app — search a Hollywood movie, get details + top-10 recommendations ([live](https://whatnext-movie.web.app/)) | JavaScript | May 2022 |
| [trailerflix](https://github.com/ibrahimsaleem/trailerflix) ★1 | React app pulling data from the TMDB API and playing trailers fetched from YouTube | JavaScript | Feb 2022 |
| [ToDo-list-react](https://github.com/ibrahimsaleem/ToDo-list-react) ★2 | Classic React to-do list | JavaScript | Apr 2022 |
| [LGMVIP-Web](https://github.com/ibrahimsaleem/LGMVIP-Web) ★2 | LetsGrowMore Virtual Internship web tasks | — | Apr 2022 |

---

## 12. Forks

### [deepseek-harness](https://github.com/ibrahimsaleem/deepseek-harness) — 🍴
**Fork of DeepSeek Harness ("Everything is a Plugin").** · TypeScript · Forked Aug 2026
- Upstream base for the Saleem Harness set and the `dsh-dashboard` observability work.

### [ai-job-search](https://github.com/ibrahimsaleem/ai-job-search) — 🍴
**Fork of an AI job-application framework built on Claude Code.** · Forked Jul 2026 — see [category 3](#3-ai-agent-harnesses-platforms--observability).

---

## 🗂️ Miscellaneous / scaffold repos

Small experiments and test repos, listed for completeness:

| Repo | Note |
|---|---|
| [testibrahim](https://github.com/ibrahimsaleem/testibrahim) ★1 | Test repository created via an AI assistant |

---

<p align="center">
  <sub>This index is maintained by hand alongside the profile README. If a repo here has grown since August 2026, its own README is the source of truth.</sub>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:7C3AED,100:4F46E5&height=100&section=footer" />
