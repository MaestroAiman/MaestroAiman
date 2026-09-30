# Hi, I'm Aiman 👋

**Software engineer who ships data & AI into real products.**
Data Science & Software Engineering student at [ENSIAS](https://ensias.um5.ac.ma) — Rabat, Morocco.

I build full-stack applications end to end and run them in production: database, API, frontend, mobile, containers and monitoring. My specialty is wiring data pipelines and LLMs into products people actually use.

🎯 **Open to a PFE (end-of-studies) internship** in Software Engineering, Data, DevOps or AI — in Morocco or abroad.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aiman%20Boutraba-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aiman-boutraba-257629321)
[![Email](https://img.shields.io/badge/Email-Contact%20me-D14836?logo=gmail&logoColor=white)](mailto:aiman_boutraba@um5.ac.ma)

---

## 🚀 Featured projects

### ☁️ [Nimbus](https://github.com/MaestroAiman/nimbus) — self-hosted personal drive
A containerized "personal Google Drive" running on a recycled laptop, with a **~1 GB RAM budget for the whole stack**. Built, deployed and used daily.

- **Streaming uploads** straight to disk and **on-the-fly ZIP downloads** — large files never sit in memory
- Per-container memory limits, **Nginx as the single entry point**, Docker healthchecks, automated backups with rotation, remote access over Tailscale
- **Strict user isolation**, verified by end-to-end tests

`NestJS` `TypeScript` `PostgreSQL` `Drizzle ORM` `Better Auth` `React` `Docker Compose` `Nginx` `Vitest`

### 🎤 [InterviewAI](https://github.com/MaestroAiman/interview-ai) — AI job-interview simulator (web + Android)
Practice technical, HR and domain interviews: the AI asks role-specific questions, scores each answer on several criteria and adapts the difficulty.

- **Multi-provider LLM architecture** — Claude API (cloud) or Ollama (local), switched by one environment variable (Strategy + Factory)
- **Structured JSON outputs** mapped to a multi-criteria feedback model, plus CV analysis from PDF
- **One JWT-secured REST API** shared by a JSF web app and a **native Android app** (Kotlin, Jetpack Compose, MVVM)
- **Observability**: Prometheus metrics and a Grafana dashboard benchmarking both AI providers

`Java 21` `Jakarta EE` `Firestore` `Kotlin` `Jetpack Compose` `Claude API` `Ollama` `Docker` `Prometheus` `Grafana`

---

## 🔒 Case studies (private code — details on request)

### 🏥 Medoc — multi-tenant SaaS for medical practice management · Invision Pixels
A platform for Moroccan medical practices (patients, scheduling, consultations, prescriptions, billing), built as three decoupled facades (web, mobile, API) around a **single source of business truth**. Main contributor in a 3-person team, 2026.

- **Multi-tenant isolation in depth**: PostgreSQL **Row-Level Security** *and* application-level filtering (Spring Security) — if one layer is bypassed, the other holds. Verified by dedicated Testcontainers integration tests.
- **Column-level AES/GCM encryption** of consultation notes: a raw SQL dump never reveals medical content
- **Claude-powered consultation assistant with a human in the loop**: patient-context chat, structured report generation and review, PDF export — never an automatic action without medical validation
- **Fine-grained access control**: JWT (access + refresh), 7 roles combined with per-page permissions; strictly intra-practice impersonation, never accessible to the platform Super-Admin (tested)
- **Real-time messaging** (WebSocket/STOMP over RabbitMQ), laboratory & pharmacy partner portals (MinIO storage), Super-Admin back-office (tenants, feature flags, GDPR requests)
- **Progressive migration** from a Next.js/Prisma v1 without interrupting the product; roadmap-driven development executed step by step with Claude Code
- Scale: ~359 Java files, 43 REST controllers, 65 Flyway migrations, ~155 TS/TSX files

`Java 21` `Spring Boot 3` `PostgreSQL (RLS)` `Flyway` `React 19` `TypeScript` `RabbitMQ` `MinIO` `Claude API` `Testcontainers` `Docker Compose`

### 👥 Radar RH — staffing platform by AI matching · Expleo Maroc (2026)
Recommends the right team for a client project from employees' skill data.
Dimensional PostgreSQL warehouse fed by an idempotent ETL · hybrid matching (exact match + **pgvector embeddings**) · deterministic, unit-tested 0–100 scoring · LLM used only for skill extraction (including from PDFs) and natural-language justification · role-based access and audit log.

`Python` `FastAPI` `PostgreSQL` `pgvector` `React` `TypeScript` `Claude API` `Ollama`

### 📊 Extracteur de matrices de compétences · Expleo Maroc (2026)
Replaced a manual consolidation: **~100 heterogeneous Excel files processed in about a minute**, ~97% of files usable despite corrupted sheets thanks to an automatic fallback, with an anomaly log instead of silent failures. It became the ETL brick of Radar RH.

`Python` `pandas` `openpyxl` `Streamlit` `Plotly`

### 🎟️ CheckIt Events — multi-tenant event platform (contribution) · 2026
Wired the Flutter attendee app to the NestJS API (session auth, signed QR tickets, notifications) and delivered an email-verified sign-up flow across every layer: Zod contract → migration → API → web form → Playwright e2e test.

`Flutter` `Dart` `NestJS` `PostgreSQL` `React` `TDD`

---

## 🛠️ Toolbox

| | Used in my projects | Coursework & labs |
|---|---|---|
| **Software** | TypeScript, Java, Python, Kotlin, Dart · Spring Boot, NestJS, Jakarta EE, FastAPI · React, Jetpack Compose, Flutter | Next.js, GraphQL |
| **DevOps** | Docker, Docker Compose, Nginx, Prometheus, Grafana, Linux, Tailscale | Kubernetes (Minikube) |
| **Data** | PostgreSQL (RLS, pgvector), Flyway, pandas, ETL, dimensional modeling, RabbitMQ | Hadoop, Spark, Hive, Kafka, time series, ML on graphs (Neo4j) |
| **AI** | LLM integration (Claude API, Ollama), embeddings & semantic search, structured outputs, human-in-the-loop design | — |

---

<sub>Currently: polishing my public repos and looking for my next engineering challenge. Let's talk!</sub>
