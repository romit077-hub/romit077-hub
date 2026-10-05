<div align="center">

# Romit Trivedi

**Local AI · Android · Full-stack Web**

Building practical tools for how I learn, work, and play.

[LinkedIn](https://www.linkedin.com/in/romit-trivedi-56a57032a/) · [Email](mailto:trivediromit7@gmail.com) · [Explore repositories](https://github.com/romit077-hub?tab=repositories)

</div>

---

## About me

I'm a **third-year BTech Computer Science student at Ganpat University — U. V. Patel College of Engineering**, based in Gujarat, India.

My projects explore practical questions: How can document answers stay traceable to their sources? Can unfinished assignments fit into the study time available? How can gaming be more accessible without owning a console?

I work across local AI, Android, and web applications, with an emphasis on understanding the architecture, debugging real failures, and validating behavior. I use AI coding tools in my workflow while strengthening my foundations in databases, data structures, operating systems, and networks.

## Featured projects

### 🧠 [NeuroVault + Synapse Active Brain](https://github.com/romit077-hub/neurovault-synapse-v0)

**Local document Q&A with source citations and human-reviewed memory updates.**  
**Status:** V0 local demo · Public source

NeuroVault indexes PDF, DOCX, and TXT documents, retrieves relevant excerpts with MiniLM embeddings and FAISS, and generates answers using Qwen 2.5 3B through Ollama. Synapse detects narrowly defined explicit fact changes and asks for a decision before replacing existing structured memory.

- Links answers to retrieved excerpts and rejects answers without valid source markers.
- Offers **Accept Update**, **Keep Existing**, or **Keep Both** for conflicting facts.
- Persists documents, memories, and review history in SQLite across restarts.

**Stack:** Python · FastAPI · React · TypeScript · SQLite · FAISS · Transformers · Ollama

**Scope:** Single-user local application after initial setup. Fact-change detection uses deterministic rules; citation markers do not guarantee answer correctness.

### 🚨 [PANIC — Deadline Enforcer](https://github.com/romit077-hub/panic_app)

**An offline Android planner that connects deadline risk with available study time.**  
**Status:** Android prototype · Public source

PANIC prioritizes unfinished tasks and schedules study sessions around availability, breaks, daily limits, and deadlines. It makes unscheduled workload visible when the available time cannot accommodate the work.

- Uses a shared deterministic risk model across the application.
- Combines a Smart Planner, workload calendar, reminders, and task analytics.
- Stores tasks locally with Room and updates the interface through Coroutines and Flow.

**Stack:** Kotlin · Jetpack Compose · Material 3 · Room · Coroutines / Flow

**Engineering focus:** Constraint-aware scheduling, reactive interfaces, and local persistence.

## More work

| Project | What it does | Stack / availability |
| --- | --- | --- |
| **LinkPulse** | URL shortening with custom slugs, QR codes, HTTP 307 redirects, and click analytics. Includes token-protected analytics and HMAC-based IP pseudonymization. | Next.js · TypeScript · Prisma · SQLite · Zod. **Private source; local prototype.** |
| **3D Developer Portfolio** | Responsive portfolio with interactive 3D typography, project filtering, reduced-motion fallbacks, and an Instant Ping endpoint designed to persist messages in D1. | Next.js · TypeScript · React Three Fiber · Tailwind CSS · Cloudflare Worker / D1. **Private source.** |
| **PSxRENT** | Console-rental web project focused on discovery, rental information, and the renter/host experience for Ahmedabad and Gandhinagar. | Next.js · React · TypeScript · Tailwind CSS. **Private source; in development.** |

## Toolkit

| Area | Tools used across my projects |
| --- | --- |
| Local AI & retrieval | Python, FastAPI, Ollama, Qwen, MiniLM, FAISS, Transformers, PyTorch |
| Android | Kotlin, Jetpack Compose, Material 3, Room, Coroutines, Flow |
| Web & interfaces | TypeScript, JavaScript, React, Next.js, Vite, Tailwind CSS, React Three Fiber |
| Data & development | SQLite, PostgreSQL, Prisma, Git, GitHub, Android Studio, pytest |

## What I'm learning

- Retrieval quality, citation handling, and explicit memory state.
- Scheduling constraints and testable application logic.
- API validation, privacy-conscious analytics, and reliable persistence.
- Clearer documentation and accessible, responsive interfaces.

## Let's connect

I'm interested in **internships, hackathons, and project collaborations** involving practical AI, Android applications, and useful web products.

[Connect on LinkedIn](https://www.linkedin.com/in/romit-trivedi-56a57032a/) · [Send an email](mailto:trivediromit7@gmail.com)

---

*Build something useful. Understand how it works. Make the next version better.*

