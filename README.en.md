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

### 🧠 Featured project: Abyss

*Personal project, in development · a local model lab on an 8 GB GPU, measured · RAG over my own documents under construction*

Abyss is the test bench where I study how local AI models behave. It runs on my PC with Ollama and is 100% local with the ONLINE switch off. It's my own frontend for Ollama, and what sets it apart is that it **measures and says what it measures**: every number is *measured*, *estimated* or *unknown*, from the data all the way to the screen.

**What already works**
- Chat actions (chat, review, think, code) with live answers and a cancel button.
- **Blind duels** between models: two answers, A and B, with the names hidden until I vote. With 10 or more votes, the recommendation comes from my votes.
- **Running on 8 GB:** one request at a time, it measures how much of the card each model takes, warns beforehand if it doesn't fit and suggests a smaller one, and unloads the models on close.
- **Governed memory:** what it generates goes in as "unreviewed" and only reaches its memory when I approve it.
- **Security of a local app:** it only listens on my PC, rejects requests from other sites, uses a session key, limits and a strict security policy, with tests.
- **No external dependencies** at runtime and 60 automated tests that run in about 30 seconds with a fake Ollama.

**The models** (Ollama, 18 installed)
- Everyday: `gemma4:e4b` (for chatting, about 84 tokens per second), `qwen3.5:4b` (the classifier that decides which model to use, about 80), `qwen3.5:9b` (for reviewing, about 56), `deepseek-r1:8b` (for thinking) and `qwen3-embedding:0.6b` (search by meaning, which runs on the CPU).
- Big ones, tested on the same card: `gpt-oss:20b`, `gemma4:26b` and `qwen3.6:35b`. They don't fit entirely in 8 GB and run at 19 to 28 tokens per second.
- I measured the speeds in October with another version of Ollama; I'm going to measure them again.

**What's next:** a RAG over my own documents that runs locally: loading and chunking them, citing the source and answering "I don't know" when there's no data, with a measurement plan defined before building (30 to 50 questions, with a held-out group). Today what exists is search by meaning over short notes, not a complete RAG.<br>
`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

<details>
<summary>🔧 How Abyss lives inside</summary>

- **Startup:** a shortcut opens Ollama if it's closed, starts a hidden Node server and opens Abyss in its own browser window. When the window closes, the server shuts down by itself and unloads the models it used.
- **Server:** plain Node.js, no external libraries or `package.json` (only Node's own modules, with built-in SQLite). It listens only on my PC, rejects requests from other sites, uses a different session key at each startup, size and rate limits and a strict security policy. What the model answers is shown as text or escaped, never as HTML.
- **Connection with Ollama:** the server talks to it through its local API: it lists the installed models, checks which one is loaded on the card, requests live answers (streaming), generates the embeddings on the CPU and loads and unloads models with each card's context. It downloads new models only from a fixed list and with a click.
- **ONLINE / OFFLINE:** it starts off. When on, it reaches Wikipedia, Wikidata, the weather, holidays, the links I paste and its own metasearch engine (SearXNG, in Docker), which forwards the query to internet search engines; only the query goes out. When off, it uses what's saved and a local Wikipedia (Kiwix, in Docker), a copy from October.
- **From the model to the screen:** the server forwards what the model generates as a continuous stream and the window renders it as it arrives.
- **Front end:** HTML, JavaScript in modules with no frameworks and SCSS compiled into a single stylesheet. A console mode (translucent black windows) and an animated beast that reacts.
- **Cards:** each action has its own editable card (goal, rules, format, model, context, temperature and token limit), with the previous version saved, and the server builds the Ollama request from it. A verifier checks the Rioplatense Spanish.
- **Measurement:** it reads the graphics card, RAM and CPU, and every number says whether it's measured, estimated or unknown. How much each model takes is measured the first time; "fits / doesn't fit" is an estimate.
- **Data:** a SQLite database with a versioned schema and full backups that are verified on restore.
- **Connection with Claude:** an MCP server with 5 tools lets Claude's agents make requests, without being able to delete, change cards or accept proposals.
- **How it was built:** with AI agents (Claude Code and Codex) from a specification that I approve, in versions, with 60 automated tests.

</details>

---

### 🚀 What I do today

In real use today: **Mascota Market** (a pet shop team) and **DGT App** (a client's fleet). **Restix** is my own product, still in development. I also automate processes with AI agents in **n8n**.

**🍽️ Restix** · *my own product, in development* · [public sample](https://github.com/sarlenguito-commits/restix-muestra) · [try it](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Management system for **bars and restaurants**: an installable Windows desktop program with tables, kitchen orders, payments with several methods and bill splitting, three cash registers with closing and reconciliation, staff, sales by channel (dine-in and PedidosYa/delivery), a protected admin PIN, automatic backups and per-device licenses. The public sample runs the same screens in the browser, with a made-up bar and automated tests on GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tasks](https://github.com/sarlenguito-commits/mascota-market)** · [see the app](https://sarlenguito-commits.github.io/mascota-market/) · *in real use*<br>
A web app used by the team of a pet shop with two stores: cleaning tasks by week and shift, shift-change notes, the owner's schedule, supplier and customer orders, and shared notes (text or checklists). Real-time data, role-based login and custom security rules.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · fleet management** · *built for a client, in use, private repository*<br>
A mobile web app that manages a fleet of motorcycles, vans and trucks: status of each vehicle, drivers by shift with their routes, tasks for drivers and mechanics, problems with diagnosis by type, spare parts stock and alerts. Five roles with their own permissions and more than 3,000 automated tests: the logic offline, the screens in the browser and the security rules against a Firebase emulator.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Automated Scouting System — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
An AI automation ecosystem (n8n + Airtable + Gemini + WhatsApp) to recruit CS2 players, with a human-in-the-loop (HITL) pause before critical actions. Final project of the AI Automation course: passed with 72%.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

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

**What's next:** taking this work to local models in Abyss, with the specification and the measurement plan written before building.

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
**Trying out:** `Docker` (I use it in Abyss for the local Wikipedia and its own search engine) and `WSL` (experimental use), `Laravel` (a small job to see how it works) and `Godot` (I have game projects in mind)

---

### 🌱 First projects

My beginnings in development: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([see the website](https://cs2databasetnl.onrender.com)), a CRM for CS2 players using the FACEIT and Steam APIs · [🥗 Healthy Calculator](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)
