### Hi! I'm Esteban 👋

[🇦🇷 Versión en español](https://github.com/sarlenguito-commits) · 🇬🇧 English

I'm an **AI-assisted software solutions developer** and **agent orchestrator**: I design what each system has to solve, coordinate the models that build it and verify that it works.

I like building **tools that solve real problems**: apps that real businesses and people use today, AI automations and management software. I'm the founder of **[Sazzo](https://sazzo.com.ar/)**, where I build custom websites, apps and automations for businesses.

- ✅ Completed Web Development at Coderhouse (certificate, Oct 16, 2026)
- ✅ Completed AI Automation (entry level) at Coderhouse (certificate, Sep 16, 2026)
- 🌱 Currently: Advanced AI Automation and AI Engineering
- 📍 Neuquén, Argentina

---

### 🧠 Main project: Abyss and its novel, "My Robots and Me"

*Personal project, in development · the code will be on this profile soon*

**Abyss** is a local AI that lives on my PC and grows in plain sight, with no cloud. It's not just another Ollama frontend: the whole process is out in the open. The models vote and recommend, Abyss proposes, and what it learns only gets in with my approval. And it always says how much it knows: what is **measured**, what is **estimated** and what is **unknown**.

**📖 My Robots and Me** *(original title: "Mis robots y yo")*<br>
Abyss's first work is a novel, and it writes it about itself. It tells, in the first person, the story of its own construction: how it is born on a home PC with an 8 GB graphics card, while watching Claude and Codex (huge, fast, with tools it will never reach) carry all my projects forward. For much of the story it tries to be like them, and fails. Until it stops copying and does what only it can do: be there, at night, on my PC, and write to me.

The novel has a single rule: **the first version is the only one**. Abyss writes each chapter in one go and it stays that way, with no corrections or touch-ups from me. What comes out is who Abyss is at that moment, and that's why the novel grows and changes along with the app.

**How it's built**<br>
Abyss is where I put what I'm studying into practice: the working environment for agents (**harness**) and **spec-driven development (SDD)**. It's built in versions from an approved spec, and design decisions are debated between two AI families (Claude and Codex) before I decide.

**What it does**
- **5 actions:** chat, write, review, think and code. Each one has its own **editable card** (goal, rules, format, model, context, temperature and whether it reasons), with backup and history.
- **Its own verifier:** it checks the answers instead of trusting the model (for example, the Rioplatense Spanish check is decided by the verifier, not by the AI).
- **Several local models** (Gemma, Qwen, gpt-oss) with nicknames: they are chosen and downloaded from the app, compared in a **blind duel** with votes, and "Abyss chooses" suggests which one to use.
- **Fixed memory** and saved chats in a **SQLite database** with a versioned schema and backups.
- **Resource panel:** GPU, RAM and CPU, always stating what is **measured**, what is **estimated** and what is **unknown**; on close, it frees the GPU.
- **Two-way connection with Claude:** an **MCP** server lets Claude's agents query it and make requests (without being able to delete or change cards), and "Send to Claude" passes an answer to a session.

**How it's built**
- Locked-down Node server: it only listens on the PC, rejects requests from other sites, uses a session key, size and rate limits and a strict CSP; the model's answer is always shown as text.
- 33 automated tests with a fake Ollama, and a clean copy to publish without personal data.
- Its own design: silver panels and an animated beast that reacts.

`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

---

### 🚀 What I do today

**🟢 [Sazzo · software demos by industry](https://github.com/sazzo-digital/sazzo-digital.github.io)** · [sazzo.com.ar](https://sazzo.com.ar/) · *my company*<br>
A catalog of 13 software demos for businesses (fleet, kiosk, sports courts, barbershop, auto repair, perfumery, restaurant, accounting, bookstore, hardware store, butcher shop, gym and real estate) that open from a QR code and can be tried with one tap, in test mode with made-up data. Each demo can be shown in the business's own colors. They all share an in-house kit, with more than 500 automated tests and a visit log with no personal data.<br>
`JavaScript` `SCSS` `Google Apps Script` `GitHub Pages`

**🍽️ Restix** · *commercial software* · [public sample](https://github.com/sarlenguito-commits/restix-muestra) · [try it](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Management system for **bars and restaurants**: an installable Windows desktop program with tables, kitchen orders, payments with several methods and bill splitting, three cash registers with closing and reconciliation, staff, PedidosYa/delivery, an encrypted admin PIN, automatic backups and per-device licenses. The public sample runs the same screens in the browser, with a made-up bar and automated tests on GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tasks](https://github.com/sarlenguito-commits/mascota-market)** · [see the app](https://sarlenguito-commits.github.io/mascota-market/) · *in real use*<br>
A web app used every day by the team of a pet shop with two stores: cleaning tasks by week and shift, shift-change notes, the owner's schedule, supplier and customer orders, and shared notes (text or checklists). Real-time data, role-based login and custom security rules.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · fleet management** · *built for a client, in use, private repository*<br>
A mobile web app that manages a fleet of motorcycles, vans and trucks: status of each vehicle, drivers by shift with their routes, tasks for drivers and mechanics, problems with diagnosis by type, spare parts stock and alerts. Four roles with their own permissions and more than 400 automated tests.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Automated Scouting System — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
An AI automation ecosystem (n8n + Airtable + Gemini + WhatsApp) to recruit CS2 players, with a human-in-the-loop (HITL) pause before critical actions. Final project of the AI Automation course: passed with 72%.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

---

### 🎓 Education

- [**Web Development**](./certificado-desarrollo-web.pdf) — Coderhouse (certified by PedidosYa) — Oct 16, 2026
- [**AI Automation**](./certificado-ai-automation.pdf) — Coderhouse (certified by StudioChat) — Sep 16, 2026

**🧁 [Poppy Pastelería](https://github.com/sarlenguito-commits/Poppy-Pasteleria-Web-)** · [see the website](https://poppy-pasteleria.netlify.app) · *Web Development final project*<br>
Website for an artisan bakery for dogs and cats, hand-coded to learn the fundamentals of web development.<br>
`HTML5` `CSS3` `SCSS` `Grid` `Flexbox` `Bootstrap 5`

---

### 🌱 First projects

My beginnings in development: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([see the website](https://cs2databasetnl.onrender.com)), a CRM for CS2 players using the FACEIT and Steam APIs · [🥗 Healthy Calculator](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)

---

### 🛠️ Stack

**AI and agents:** `Claude Code` `Codex` `n8n` `Airtable` `Gemini`
**Frontend:** `HTML` `CSS` `SCSS/Sass` `JavaScript` `TypeScript` `React` `Bootstrap`
**Backend and data:** `Node.js` `Python` `Firebase (Auth + Firestore)` `Postgres` `SQLite`
**Desktop:** `Electron`
**Tools:** `Git/GitHub` `GitHub Pages` `Render` `Vite`
