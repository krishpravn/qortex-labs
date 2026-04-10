# Phoenix TestAI

**AI-Native Quality Intelligence Platform**

From every failure, intelligence rises. 6 autonomous AI agents, 11 testing types, MCP protocol integration, Playwright + Vibium execution, and complete test lifecycle management. Self-hosted, zero vendor lock-in.

🔗 **Showcase:** [krishpravn.github.io/qortex-labs/phoenix-testai/](https://krishpravn.github.io/qortex-labs/phoenix-testai/)

---

## What Is Phoenix TestAI?

Phoenix TestAI is an AI-native test management and execution platform built from the ground up. It combines test execution (Playwright), AI intelligence (6 autonomous agents), and complete test lifecycle management (Requirements, Test Cases, Test Plans, Defects) into one self-hosted platform.

Unlike tools that bolt AI onto existing features, Phoenix was designed with AI at the core. Every failure triggers an intelligent response: triage, learning, strategy adjustment, and automated action.

---

## Platform Numbers

| Metric | Count |
|---|---|
| Source Files | 230 |
| Lines of Code | 37,000+ |
| Prisma Models | 31 |
| API Routes | 80 |
| AI Tools | 26 (dynamic based on MCP connections) |
| AI Agents | 6 |
| Report Types | 8 |
| Testing Types | 11 (2 built, 9 planned) |
| Design Themes | 4 |
| RBAC Roles | 5 |

---

## Key Capabilities

### AI Intelligence
- **LLM Router** with 5 providers (OpenRouter, Anthropic, OpenAI, Ollama, Azure), 3-tier fallback, and task-aware routing
- **26-Tool AI Chat** with dynamic tool loading: 13 database tools + 4 browser tools (Playwright MCP) + 4 code tools (Filesystem MCP) + 5 repo tools (GitHub MCP)
- **6 Autonomous Agents** (Triage, Discovery, Strategy, Learning, Generator, Executor) with ReAct reasoning, confidence scoring, and human-in-loop approval
- **Self-Healer** covering ALL 6 failure categories: Selectors (28%), Timing (25%), Runtime (15%), Test Data (15%), Visual (10%), Interactions (7%)
- **AI Test Generator** with 3 modes: from text, from URL, from existing test. Interactive checklist review before saving
- **Cost Observatory** with budget tracking, provider/model/task breakdowns, and optimization recommendations

### Test Management
- **Requirements** with Jira import via Rovo MCP, AI expansion of vague requirements, MoSCoW prioritization
- **Test Cases** with step-by-step definitions, automation status linking, requirement tracing
- **Test Plans** with manual execution interface, progress tracking, assignee management
- **Defects** with 7-status workflow (New through Closed/Rejected), severity/priority classification
- **Requirements Traceability Matrix** linking Requirements, Test Cases, and Defects

### Execution
- **Playwright** (active): Chromium, Firefox, WebKit. Headed/headless. 6 device profiles. Live SSE streaming. AI failure analysis on every failure
- **Vibium** (planned): AI-native browser with WebDriver BiDi, visual regression, exploratory testing, page object generation
- **Run Config Dialog**: Browser, device, mode, workers, retries selection before every run

### MCP Integration
- **Playwright MCP**: 18 browser automation capabilities (navigate, click, fill, screenshot, snapshot)
- **Filesystem MCP**: Read test files, search code patterns, list directory structure
- **GitHub MCP**: PR diffs, repo files, code search, commits, issues
- **Server Registry**: Add, connect, disconnect MCP servers through Settings UI with quick-add presets

### Enterprise
- **5-Role RBAC**: Owner, Admin, Lead, Tester, Viewer with 16 resource permissions
- **Scheduling Engine**: Cron expressions, event-triggered, AI-driven smart scheduling
- **Notifications**: Email + Webhook with rate limiting, quiet hours, severity thresholds
- **8 Report Types**: Execution Summary, Coverage Matrix, Defect Summary, Flake Intelligence, AI Performance, Release Readiness, Compliance Evidence, Sprint Summary
- **Compliance Dashboards**: SOC 2, HIPAA, GDPR, ISO 27001
- **Audit Trail**, **User Management**, **Synthetic Monitor**, **Allure Import**

### Design
- **4 Themes**: Sapphire (blue), Ember (warm), Violet (purple), Teal (green)
- **Plus Jakarta Sans** + **JetBrains Mono**
- **14 configurable dashboard widgets** with drag-and-drop layout
- **Live Commentary**: AI narrates test execution in real-time

---

## Testing Types

| Type | Status | Technology |
|---|---|---|
| Web E2E | Built | Playwright |
| Cross-Browser & Device | Built | Chromium, Firefox, WebKit + 6 devices |
| Exploratory | Planned | AI-assisted guided sessions |
| Performance | Planned | k6, Lighthouse |
| Security | Planned | OWASP scanning |
| Visual Regression | Planned | Screenshot comparison with AI diff |
| API Protocol | Planned | REST, GraphQL, WebSocket, gRPC via MCP |
| Accessibility | Planned | WCAG compliance |
| Contract | Planned | OpenAPI spec validation |
| Data-Driven | Planned | CSV/JSON parameterization |
| Chaos & Resilience | Planned | Fault injection, recovery testing |

---

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | Next.js 15, React 19, TypeScript 5, Tailwind CSS v4, shadcn/ui, Zustand 5 |
| AI | OpenRouter, Anthropic, OpenAI, Ollama, Azure via LLM Router |
| Agents | 6 agents with ReAct loop, EventEmitter orchestrator, Proposal system |
| MCP | @modelcontextprotocol/sdk, STDIO transport, Playwright/Filesystem/GitHub servers |
| Execution | Playwright with child_process spawning, SSE streaming |
| Auth | Auth.js (NextAuth) with JWT sessions, bcryptjs |
| Database | Prisma ORM, SQLite (dev), PostgreSQL (prod) |
| Reports | 8 HTML templates, Recharts, Allure parser |
| Scheduling | node-cron, event-triggered, Nodemailer |

---

## Architecture

```
┌─────────────────────────────────────────────┐
│  Frontend (Next.js 15 + React 19)           │
│  27 pages, 4 themes, widget configurator    │
├─────────────────────────────────────────────┤
│  AI Intelligence Layer                       │
│  LLM Router → 5 providers → Cost tracking   │
├─────────────────────────────────────────────┤
│  Agent Framework                             │
│  6 agents → ReAct → Proposals → Execution   │
├─────────────────────────────────────────────┤
│  MCP Integration                             │
│  Playwright + Filesystem + GitHub servers    │
├─────────────────────────────────────────────┤
│  Enterprise Layer                            │
│  RBAC + Scheduling + Notifications + Reports │
├─────────────────────────────────────────────┤
│  Execution Engine                            │
│  Playwright runner + SSE + AI analysis       │
├─────────────────────────────────────────────┤
│  Data Layer                                  │
│  31 Prisma models + Event bus + Audit trail  │
└─────────────────────────────────────────────┘
```

---

## Build Phases

| Phase | Name | Status | Sessions |
|---|---|---|---|
| P0-P2 | Foundation + Execution + Intelligence | Complete | 12 |
| P3 | AI Layer (Router, Chat, Healer, Generator, KB) | Complete | 6 |
| P4 | Test Management (Req, TC, Defects, Plans, RTM) | Complete | 5 |
| P5 | Agentic Intelligence (6 agents, event bus, REST API) | Complete | 14 |
| P6 | Enterprise (RBAC, scheduling, reports, analytics, compliance) | Complete | 16 |
| P7 | Expansion (MCP, Playwright/Filesystem/GitHub servers) | In Progress | 4 of 12 |
| P8 | Polish & Hardening | Planned | — |

---

## About

Built by **Krishna Praveen Manchala**, Senior QA Manager with 17+ years of experience. Part of the [Qortex Labs](https://krishpravn.github.io/qortex-labs/) portfolio of AI-powered quality engineering tools.

📧 krishpravn@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/krishpravn)

---

## Other Products

- **[API Qortex](https://krishpravn.github.io/api-qortex/)** — AI-powered API testing and documentation platform
- **Qortex Sandbox** — Experimentation playground (in development)
- **API Sentinel** — API failure intelligence platform (documented, build pending)

---

## License

MIT
