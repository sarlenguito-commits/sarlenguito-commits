### Hi! I'm Esteban 👋

[🇦🇷 Versión en español](https://github.com/sarlenguito-commits) · 🇬🇧 English

I'm a **student of AI Engineering focused on model orchestration and evaluation**. I'm interested in how different models behave, how to make them work together and how to check that what they answer is correct. In practice, I build software with AI: I design what each system has to solve, coordinate the models that build it and verify that it works.

I like building **tools that solve real problems**: apps that real businesses and people use today, AI automations and management software.

- ✅ Completed Web Development at Coderhouse (certificate, Oct 16, 2026)
- ✅ Completed AI Automation (entry level) at Coderhouse (certificate, Sep 16, 2026)
- 🌱 Currently: Advanced AI Automation and AI Engineering
- 🔎 Focus: RAG systems (a model that answers from my own documents, with results you can measure)
- 📍 Neuquén, Argentina

---

### 🚀 What I do today

In real use today: **Mascota Market** (a pet shop team, every day) and **DGT App** (a client's fleet). **Restix** is commercial software. I also automate processes with AI agents in **n8n**.

**🍽️ Restix** · *commercial software* · [public sample](https://github.com/sarlenguito-commits/restix-muestra) · [try it](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Management system for **bars and restaurants**: an installable Windows desktop program with tables, kitchen orders, payments with several methods and bill splitting, three cash registers with closing and reconciliation, staff, PedidosYa/delivery, an encrypted admin PIN, automatic backups and per-device licenses. The public sample runs the same screens in the browser, with a made-up bar and automated tests on GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tasks](https://github.com/sarlenguito-commits/mascota-market)** · [see the app](https://sarlenguito-commits.github.io/mascota-market/) · *in real use*<br>
A web app used every day by the team of a pet shop with two stores: cleaning tasks by week and shift, shift-change notes, the owner's schedule, supplier and customer orders, and shared notes (text or checklists). Real-time data, role-based login and custom security rules.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · fleet management** · *built for a client, in use, private repository*<br>
A mobile web app that manages a fleet of motorcycles, vans and trucks: status of each vehicle, drivers by shift with their routes, tasks for drivers and mechanics, problems with diagnosis by type, spare parts stock and alerts. Four roles with their own permissions and more than 3,000 automated tests: the logic offline, the screens in the browser and the security rules against a Firebase emulator.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Automated Scouting System — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
An AI automation ecosystem (n8n + Airtable + Gemini + WhatsApp) to recruit CS2 players, with a human-in-the-loop (HITL) pause before critical actions. Final project of the AI Automation course: passed with 72%.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

**🧠 Abyss** · *personal project, in development · the code will be on this profile soon*<br>
A local AI that lives on my PC, with no cloud. Everything it generates goes in as "unreviewed" and only reaches its memory when I approve it; the models are compared in blind duels, where I vote for which one answered better. It's where I practice the working environment for agents (harness) and spec-driven development (SDD). Its first work is a novel it writes about itself.<br>
`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

---

### 🔎 My specialization focus: RAG

I want to specialize in **RAG** (retrieval-augmented generation): having a model answer with information from my own documents, citing where it came from and saying "I don't know" when it doesn't have it. I look for, analyze and build systems like this, and what interests me most is that **you can measure whether they work**.

**What I've already built:** an agent in **n8n** that answers a real estate agency's inquiries from its FAQ document (a practice case from the course, with made-up data).
- **Ingestion:** the document is parsed with **LlamaCloud** (titles and tables preserved) and split into chunks of 1,500 characters with 200 characters of overlap.
- **Vectors:** embeddings with **Gemini** (`gemini-embedding-001`, 3,072 dimensions) stored in **Supabase (Postgres with pgvector)**, with row-level security (RLS) and permissions only for the service role.
- **Search:** a custom SQL function with a **minimum similarity score of 0.62** and **Top-K 3**, tuned to balance precision and token cost.
- **Answer:** the agent cites its source and says "I don't know" when the search returns nothing useful, instead of making something up.
- **Measurement:** 5 questions over 3 rounds, adjusting between them: 60%, 60% and 80% correct. It's a small sample: it helped me see where it failed, not to measure precisely.

**How I work:** I measure the similarity score of each chunk, tune the parameters instead of keeping the defaults and separate what fails in the search from what fails in the model's answer (for example, a requirement the model added that wasn't in the document).

**What I'm learning now (AI Engineering):** embeddings and similarity, chunking strategies, local vector databases with **ChromaDB**, scalable cloud RAG with **Pinecone**, hybrid retrieval, retrieval metrics and observability with **LangSmith** and **Arize Phoenix**.<br>
`n8n` `LlamaCloud` `Supabase` `pgvector` `Gemini embeddings` `ChromaDB` `Pinecone`

---

### 🔬 What I'm exploring

I spend a good part of my time studying how AI models behave and testing whether they can work together. I have them review and debate each other from the command line (CLI) and I keep a record of what each one sees that the others don't, to learn what each model is good for.

What I'm after:
- Models from different families giving each other second opinions: one proposes, another reviews and the final decision is mine.
- Verifying instead of trusting: an answer isn't good because it sounds good, it's checked with tests, with a verifier or by hand.
- Keeping everything on record: what each model said, what was decided and why, so I can compare over time.
- Practicing with real projects what I study: the working environment for agents (harness) and spec-driven development (SDD).

---

### 🎓 Education at Coderhouse

**Web Development** · 30 hours · [certificate](./certificado-desarrollo-web.pdf) (certified by PedidosYa) · Oct 16, 2026<br>
Semantic HTML5, CSS3, box model, Flexbox, CSS Grid and media queries, Bootstrap 5, Git and GitHub with continuous deployment, SCSS, animations (transitions and keyframes), SEO, domains and servers, and the basics of working as a freelance developer. Final project: Poppy Pastelería.<br>
`HTML5` `CSS3` `SCSS` `Bootstrap 5` `Git` `GitHub Pages`

**AI Automation (entry level)** · [certificate](./certificado-ai-automation.pdf) (certified by StudioChat) · Sep 16, 2026<br>
Flow design (triggers, inputs and outputs), no-code and low-code, **Make** (routers, filters, JSON, error handling and the OpenAI API), **n8n** (agents with LangChain, HTTP Request, loops and sub-workflows), Gmail, Slack and WhatsApp API, the Claude API (batches, prompt caching and MCP), agents with RAG memory, human-in-the-loop (HITL) and dashboards. Final project: the CS2 scouting system.<br>
`Make` `n8n` `Airtable` `Gemini` `WhatsApp API` `Claude API` `MCP`

**Advanced AI Automation** · in progress · [deliveries on GitHub](https://github.com/sarlenguito-commits/ia-automation-avanzado)<br>
Autonomous agents in n8n, multi-agent architecture (Manager-Worker, Planner and sub-workflows), guardrails, memory and persistence, OAuth2 integrations (Gmail, HubSpot and Slack), RAG over documents, voice (bots that listen and speak, with Whisper), industry-specific agents, automatic evaluation (AI as a judge), governance, token costs and observability.<br>
`n8n` `OAuth2` `RAG` `Whisper` `HubSpot` `Slack`

**AI Engineering** · in progress · [first pre-delivery, passed with 91%](https://github.com/sarlenguito-commits/ia-engineer-1)<br>
Asynchronous Python 3.12, LLM clients, chains with LangChain, structured validation, embeddings and chunking, vector databases (ChromaDB and Pinecone), RAG, agents with LangGraph (tools, ReAct cycles and checkpoints), multi-agent systems with the supervisor pattern, observability (Arize Phoenix and LangSmith) and production APIs with FastAPI and Redis.<br>
`Python` `LangChain` `LangGraph` `ChromaDB` `Pinecone` `FastAPI`

**🧁 [Poppy Pastelería](https://github.com/sarlenguito-commits/Poppy-Pasteleria-Web-)** · [see the website](https://poppy-pasteleria.netlify.app) · *Web Development final project*<br>
Website for an artisan bakery for dogs and cats, built to learn the fundamentals of web development.<br>
`HTML5` `CSS3` `SCSS` `Grid` `Flexbox` `Bootstrap 5`

---

### 🧰 Tools and experience

What I have installed and use in my projects and courses.

**AI automation:** I work with **n8n** and **Make** to build flows with AI agents: they read emails, register contacts in a CRM, notify on Slack and leave drafts for a person to review before sending.
**AI and agents:** `Claude Code` `Codex` `n8n` `Make` `Gemini` `MCP`
**Local models (Ollama):** `Gemma 4` `Qwen 3.5` `DeepSeek R1` `Qwen3 Embedding`
**Voice:** `Whisper` `faster-whisper` (bots that listen and speak)
**APIs and connections:** `REST` `Webhooks` `HTTP Request` `OAuth2` `Gmail` `Slack` `HubSpot` `WhatsApp API` `Airtable` `Gemini` `Groq (gpt-oss)` `Claude API`
**Languages:** `JavaScript` `TypeScript` `Python` `HTML` `CSS` `SCSS/Sass` `PowerShell`
**Frontend and desktop:** `React` `Bootstrap` `Vite` `Electron` `PWA`
**Backend and cloud:** `Node.js` `Firebase (Auth + Firestore + Hosting)` `Cloudflare Workers`
**Databases:** `SQLite` `Firestore` `Postgres` `Airtable`
**Testing and quality:** `Vitest` `automated tests` `Firebase emulator` `GitHub Actions` `accessibility (Axe)`
**Deployment:** `GitHub Pages` `Firebase Hosting` `Netlify` `Render`
**Tools:** `Git/GitHub` `GitHub CLI` `VS Code` `Live Server` `Prettier` `Error Lens` `SQLite Viewer` `REST Client` `Draw.io`
**Learning now:** `LangChain` `LangGraph` `ChromaDB` `Pinecone` `FastAPI` `Redis`
**Trying out:** `Docker` and `WSL` (experimental use), `Laravel` (a small job to see how it works) and `Godot` (I have game projects in mind)

---

### 🌱 First projects

My beginnings in development: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([see the website](https://cs2databasetnl.onrender.com)), a CRM for CS2 players using the FACEIT and Steam APIs · [🥗 Healthy Calculator](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)
