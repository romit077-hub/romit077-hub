<!-- ROMIT TRIVEDI · GITHUB PROFILE -->
<!-- Profile repository: romit077-hub/romit077-hub -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:7C3AED,100:DB2777&height=210&section=header&text=Romit%20Trivedi&fontSize=48&fontAlignY=38&animation=fadeIn&fontColor=ffffff&desc=Curiosity%20into%20code.%20Ideas%20into%20products.&descAlignY=61&descSize=17" width="100%" alt="Romit Trivedi — Curiosity into code. Ideas into products." />
</p>

<p align="center">
  <b>Local AI · Android · Full-stack Web</b><br/>
  I build tools for how I learn, work, and play.
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=19&duration=2800&pause=1200&color=22D3EE&center=true&vCenter=true&width=620&height=40&lines=BTech+CSE+Student+%7C+Gujarat%2C+India;NeuroVault+%2B+Synapse+V0+%E2%80%94+Complete;Building+Android+apps+and+web+products;Learning+through+real+projects" width="620" alt="BTech CSE student in Gujarat, India. NeuroVault + Synapse V0 is complete. Building Android and web projects." />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/romit-trivedi-56a57032a/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Connect with Romit on LinkedIn" /></a>
  <a href="https://github.com/romit077-hub?tab=repositories"><img src="https://img.shields.io/badge/Explore_Projects-181717?style=for-the-badge&logo=github&logoColor=white" alt="Explore Romit's GitHub repositories" /></a>
  <a href="https://github.com/romit077-hub/neurovault-synapse-v0"><img src="https://img.shields.io/badge/Latest_Build-NeuroVault_V0-7C3AED?style=for-the-badge" alt="Latest project: NeuroVault + Synapse V0" /></a>
</p>

<p align="center">
  <a href="#selected-projects">Selected projects</a> ·
  <a href="#toolkit">Toolkit</a> ·
  <a href="#current-focus">Current focus</a> ·
  <a href="#lets-connect">Let's connect</a>
</p>

---

## A little about me

I'm **Romit**, a **third-year BTech Computer Science student** at **Ganpat University — U. V. Patel College of Engineering**, based in Gujarat, India.

My projects start with practical questions: Can I keep track of changing information? Can my remaining assignments fit into my study time? Can gaming be more accessible without owning a console?

I'm building experience across **local AI systems, Android applications and web development**, while strengthening my foundations in data structures, databases, operating systems and computer networks. I use AI coding tools in my workflow and work on understanding the architecture, debugging failures and validating behavior on real hardware.

> **Build something useful. Understand how it works. Make the next version better.**

## Selected projects

### 🧠 NeuroVault + Synapse Active Brain

**A local knowledge vault that answers from your documents and flags changing facts for your review.**

<p>
  <img src="https://img.shields.io/badge/Stage-V0_Complete-22C55E?style=flat-square" alt="V0 complete" />
  <img src="https://img.shields.io/badge/Runtime-Local_AI-06B6D4?style=flat-square" alt="Local AI runtime" />
  <img src="https://img.shields.io/badge/Memory-Human_Reviewed-8B5CF6?style=flat-square" alt="Human review of memory updates" />
</p>

**NeuroVault** handles document ingestion, semantic retrieval and cited Q&A. **Synapse** keeps structured facts alongside the source archive and flags supported updates or contradictions before replacing existing memory.

- **Document ingestion:** index text-based PDF, DOCX and TXT files with source references.
- **Semantic search:** retrieve relevant excerpts using MiniLM embeddings and FAISS.
- **Local Q&A:** generate answers with **Qwen 2.5 3B through Ollama**, using the retrieved evidence.
- **Citation checks:** validate retrieved-source markers, attempt one constrained repair when needed, and reject answers that still lack valid citations.
- **Reviewable changes:** rule-based detection identifies supported fact changes, such as a revised assignment deadline. Choose **Accept Update**, **Keep Existing** or **Keep Both**.
- **Persistent history:** SQLite retains documents, structured memories and review decisions across restarts, including active and superseded facts.

> **Verified demo:** an assignment deadline changes from **14 October to 18 October**. Synapse flags the update; accepting it makes 18 October active while preserving 14 October as superseded history.

**V0 validation · 1 October 2026:** **31 backend tests passed**, with manual Windows checks for ingestion, retrieval, single- and multi-source citations, update acceptance and persistence after restart.

**Stack:** `Python` · `FastAPI` · `React` · `TypeScript` · `Vite` · `Tailwind CSS` · `SQLite` · `FAISS` · `MiniLM` · `Ollama`

**Engineering focus:** evidence retrieval, citation handling, explicit memory state and human control over changing facts.

<details>
<summary><b>A closer look at the V0 design</b></summary>

| Layer | Role |
| --- | --- |
| Document processing | Extract and chunk text while retaining source references. |
| MiniLM + FAISS | Create normalized 384-dimensional embeddings and retrieve similar chunks. |
| Ollama + Qwen 2.5 3B | Generate a natural-language answer from the retrieved excerpts. |
| Citation validation | Check returned markers against sources supplied for that question. |
| Synapse | Compare supported explicit facts and queue updates or contradictions for review. |
| SQLite | Persist documents, embeddings, memories, sources and alerts. |

The embedding model runs through **Transformers + PyTorch**. Synapse's current fact classification uses deterministic rules; Qwen handles answer generation.

Accepting a memory update preserves the older source document, so retrieval can still explain the history of a change. Normal use runs locally after the initial dependency and model downloads.

**Current scope:** a single-user local MVP. OCR, cloud sync and autonomous agents are outside the completed V0.
and please keep in mind i am soon releasing the exe app for window , the reason it is not there because its just v0.....

</details>

**[Explore NeuroVault + Synapse →](https://github.com/romit077-hub/neurovault-synapse-v0)**

---

### 🚨 PANIC — Deadline Enforcer

**Can your remaining work actually fit before the deadline?**

<p>
  <img src="https://img.shields.io/badge/Stage-Portfolio_Demo-F59E0B?style=flat-square" alt="Portfolio demo" />
  <img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Android" />
  <img src="https://img.shields.io/badge/Core-Offline_First-06B6D4?style=flat-square" alt="Offline-first core" />
</p>

An Android deadline planner that connects task management, study availability and workload risk in one local workflow.

- **Deadline risk:** deterministic scoring based on deadlines, remaining work and priority.
- **Smart Planner:** study sessions arranged around availability, breaks and daily limits.
- **Workload feedback:** highlights tasks that cannot fit into the available study time.
- **Local persistence:** Room-backed tasks, a workload calendar and task-based analytics.

**Stack:** `Kotlin` · `Jetpack Compose` · `Material 3` · `Room` · `Coroutines / Flow`

**Engineering focus:** constraint-aware scheduling, reactive UI and testable domain logic. The core planner uses deterministic rules.

**[Explore PANIC →](https://github.com/romit077-hub/panic_app)**

---

### 🔗 LinkPulse — URL Shortening & Click Analytics

**Short links with useful analytics and deliberate data-handling choices.**

A full-stack URL shortener with custom slugs, QR codes, HTTP 307 redirects and click analytics.

- **Link management:** random or custom short URLs with database-backed slug uniqueness.
- **Analytics:** click events and device distribution, with token-protected private analytics.
- **Data minimization:** HMAC-SHA256 IP pseudonymization and hostname-level referrer storage.
- **Request controls:** destination validation, API rate limiting and defensive HTTP headers.

**Stack:** `Next.js` · `React` · `TypeScript` · `Prisma` · `SQLite` · `Zod`

**Architecture:** Next.js route handlers validate requests, use Prisma for persistence, and coordinate redirects with click-event recording.

**Engineering focus:** input validation, redirect behavior, analytics storage and privacy trade-offs.

**[Explore LinkPulse →](https://github.com/romit077-hub/url-shortener-pro)**

---

### 🎮 PSxRENT — Console Rental Platform

**Gaming without the upfront cost of owning a console.**

<p>
  <img src="https://img.shields.io/badge/Stage-In_Development-F59E0B?style=flat-square" alt="In development" />
  <img src="https://img.shields.io/badge/Focus-Ahmedabad_%26_Gandhinagar-8B5CF6?style=flat-square" alt="Initial focus: Ahmedabad and Gandhinagar" />
</p>

A web project aimed at connecting gamers with console owners and rental shops. I'm developing the experience around **renters and hosts**, with clear console discovery, rental information and pricing.

**Stack:** `TypeScript` · `Next.js` · `React` · `Tailwind CSS` · `Prisma` · `PostgreSQL`

**Engineering focus:** full-stack application structure, rental workflows and product usability.

**[View web preview →](https://psxrent-m024rzlh6-ps-x-rent.vercel.app/)** · **[Follow PSxRENT →](https://instagram.com/psxrent)**

## Toolkit

Tools I use across my projects and continue to learn.

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
</p>

| Area | Project toolkit |
| --- | --- |
| Local AI & retrieval | Python, FastAPI, Ollama, Qwen, MiniLM, FAISS, Transformers, PyTorch |
| Android | Kotlin, Jetpack Compose, Material 3, Room, Coroutines, Flow |
| Web | TypeScript, JavaScript, React, Next.js, Vite, Tailwind CSS |
| Data & development | SQLite, PostgreSQL, Prisma, Git, GitHub, Android Studio, pytest |

## Current focus

- **NeuroVault + Synapse:** documenting and showcasing the completed V0 and its verified behavior.
- **PANIC:** refining the demo, usability and testing on real devices.
- **PSxRENT:** developing the core rental experience into a usable MVP.
- **Engineering foundations:** clearer code, useful tests, data structures and system design basics.

<details>
<summary><b>📊 Public GitHub activity</b></summary>

<br/>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=romit077-hub&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" width="49%" alt="Romit's public GitHub statistics" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=romit077-hub&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" width="49%" alt="Language distribution across Romit's public repositories" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=romit077-hub&bg_color=1a1b27&color=70a5fd&line=38bdae&point=bf91f3&area=true&hide_border=true" width="100%" alt="Romit's GitHub contribution activity graph" />
</p>

<!-- Optional third-party cards; availability depends on their hosting services. -->

</details>

## Let's connect

I'm interested in **internships, hackathons and project collaborations** around student tools, Android apps, gaming products and practical AI.

Have a useful problem, an idea to test or feedback on one of my projects? I'd like to hear it.

<p align="center">
  <a href="https://www.linkedin.com/in/romit-trivedi-56a57032a/"><b>LinkedIn</b></a> ·
  <a href="https://github.com/romit077-hub?tab=repositories"><b>GitHub projects</b></a> ·
  <a href="https://instagram.com/romit_2.11">Instagram</a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:DB2777,50:7C3AED,100:06B6D4&height=100&section=footer" width="100%" alt="Cyan, violet and pink gradient footer" />
</p>
