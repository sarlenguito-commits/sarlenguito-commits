### ¡Hola! Soy Esteban 👋

🇦🇷 Español · [🇬🇧 English version](https://github.com/sarlenguito-commits/sarlenguito-commits/blob/main/README.en.md)

Soy **estudiante de AI Engineering con foco en orquestación y evaluación de modelos**. Me interesa entender cómo se comportan los distintos modelos, cómo hacerlos trabajar juntos y cómo comprobar que lo que responden es correcto. En la práctica, desarrollo software con IA: diseño qué tiene que resolver cada sistema, coordino a los modelos que lo construyen y verifico que funcione.

Me gusta construir **herramientas que resuelven problemas reales**: apps que hoy usan negocios y personas de verdad, automatizaciones con IA y software de gestión.

- ✅ Terminé Desarrollo Web en Coderhouse (certificado, 16/10/2026)
- ✅ Terminé IA Automation (nivel inicial) en Coderhouse (certificado, 16/09/2026)
- 🌱 Actualmente: IA Automation Avanzado y AI Engineering
- 🔎 Foco: sistemas RAG (que un modelo responda con mis documentos y se pueda medir)
- 📍 Neuquén, Argentina

---

### 🚀 Lo que hago hoy

En uso real hoy: **Mascota Market** (el equipo de un pet shop, todos los días) y **DGT App** (la flota de un cliente). **Restix** es software comercial. También automatizo procesos con agentes de IA en **n8n**.

**🍽️ Restix** · *software comercial* · [muestra pública](https://github.com/sarlenguito-commits/restix-muestra) · [probarla](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Sistema de gestión para **bares y restaurantes**: programa de escritorio instalable para Windows, con mesas, comandas a cocina, cobro con varios medios de pago y división de cuentas, tres cajas con cierre y arqueo, personal, Pedidos Ya/Delivery, PIN de administrador cifrado, copias de seguridad automáticas y licencias por equipo. La muestra pública corre las mismas pantallas en el navegador, con un bar inventado y pruebas automáticas en GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tareas](https://github.com/sarlenguito-commits/mascota-market)** · [ver app](https://sarlenguito-commits.github.io/mascota-market/) · *en uso real*<br>
App web que usa todos los días el equipo de un pet shop con dos locales: tareas de limpieza por semana y turno, notas de cambio de turno, agenda de la dueña, pedidos a proveedores y de clientes, y notas compartidas (texto o listas para tildar). Datos en tiempo real, login por roles y reglas de seguridad propias.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · gestión de flota** · *hecha para un cliente, en uso, repositorio privado*<br>
App web para celular que lleva una flota de motos, camionetas y camiones: estado de cada vehículo, choferes por turno con sus recorridos, tareas para choferes y mecánicos, problemas con diagnóstico por tipo, stock de repuestos y avisos. Cuatro roles con permisos propios y más de 3.000 pruebas automáticas: la lógica sin conexión, las pantallas en el navegador y las reglas de seguridad contra un emulador de Firebase.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Sistema de Scouting Automatizado — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
Ecosistema de automatización con IA (n8n + Airtable + Gemini + WhatsApp) para reclutar jugadores de CS2, con punto de pausa humano (HITL) antes de acciones críticas. Proyecto final del curso de Automatización con IA: aprobado con 72 %.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

**🧠 Abyss** · *proyecto personal, en desarrollo · el código va a estar pronto en este perfil*<br>
IA local que vive en mi PC y crece a la vista, sin nube: los modelos votan, Abyss propone y lo que aprende entra solo con mi aprobación. Es donde practico el entorno de trabajo de los agentes (harness) y el desarrollo guiado por especificaciones (SDD). Su primer trabajo es una novela que escribe sobre sí misma.<br>
`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

---

### 🔎 Mi línea de especialización: RAG

Quiero especializarme en **RAG** (generación aumentada por recuperación): que un modelo responda con información de documentos propios, citando de dónde la sacó y diciendo "no sé" cuando no la tiene. Busco, analizo y construyo sistemas de este tipo, y lo que más me interesa es que **se pueda medir si funcionan**.

**Lo que ya construí:** un agente en **n8n** que responde consultas de una inmobiliaria a partir de su documento de preguntas frecuentes (caso de práctica del curso, con datos inventados).
- **Ingesta:** el documento se parsea con **LlamaCloud** (títulos y tablas conservados) y se divide en fragmentos de 1.500 caracteres con 200 de solapamiento.
- **Vectores:** embeddings con **Gemini** (`gemini-embedding-001`, 3.072 dimensiones) guardados en **Supabase (Postgres con pgvector)**, con seguridad por filas (RLS) y permisos solo para el servicio.
- **Búsqueda:** una función SQL propia con **puntaje mínimo de similitud 0,62** y **Top-K 3**, calibrados para equilibrar precisión y costo de tokens.
- **Respuesta:** el agente cita la fuente y responde "no sé" cuando la búsqueda no devuelve nada que sirva, en lugar de inventar.
- **Medición:** 5 preguntas en 3 rondas, ajustando entre una y otra: 60 %, 60 % y 80 % de aciertos. Es una muestra chica: me sirvió para ver dónde fallaba, no para medir con precisión.

**Cómo lo trabajo:** mido el puntaje de similitud de cada fragmento, calibro los parámetros en vez de dejar los de fábrica y separo lo que falla en la búsqueda de lo que falla en la respuesta del modelo (por ejemplo, un requisito que el modelo agregó y no estaba en el documento).

**Lo que estoy aprendiendo ahora (AI Engineering):** embeddings y similitud, estrategias de chunking, bases vectoriales locales con **ChromaDB**, RAG escalable en la nube con **Pinecone**, recuperación híbrida, métricas de recuperación y observabilidad con **LangSmith** y **Arize Phoenix**.<br>
`n8n` `LlamaCloud` `Supabase` `pgvector` `Gemini embeddings` `ChromaDB` `Pinecone`

---

### 🔬 Lo que estoy explorando

Paso buena parte de mi tiempo estudiando cómo se comportan los modelos de IA y probando si pueden trabajar juntos. Hago que se revisen y debatan entre sí desde la línea de comandos (CLI) y llevo un registro de lo que cada uno ve y los otros no, para saber en qué sirve cada modelo.

Lo que busco con eso:
- Que modelos de distintas familias se den segundas opiniones: uno propone, otro revisa y la decisión final es mía.
- Verificar en vez de confiar: una respuesta no es buena porque suene bien, se comprueba con pruebas, con un verificador o a mano.
- Dejar todo registrado: qué opinó cada modelo, qué se decidió y por qué, para poder comparar con el tiempo.
- Practicar con proyectos reales lo que estudio: el entorno de trabajo de los agentes (harness) y el desarrollo guiado por especificaciones (SDD).

---

### 🎓 Formación en Coderhouse

**Desarrollo Web** · 30 horas · [certificado](./certificado-desarrollo-web.pdf) (certificado por PedidosYa) · 16/10/2026<br>
HTML5 semántico, CSS3, modelo de caja, Flexbox, CSS Grid y media queries, Bootstrap 5, Git y GitHub con despliegue continuo, SCSS, animaciones (transiciones y keyframes), SEO, dominios y servidores, y bases del trabajo como desarrollador freelance. Proyecto final: Poppy Pastelería.<br>
`HTML5` `CSS3` `SCSS` `Bootstrap 5` `Git` `GitHub Pages`

**IA Automation (nivel inicial)** · [certificado](./certificado-ai-automation.pdf) (certificado por StudioChat) · 16/09/2026<br>
Diseño de flujos (disparadores, entradas y salidas), no-code y low-code, **Make** (routers, filtros, JSON, manejo de errores y API de OpenAI), **n8n** (agentes con LangChain, HTTP Request, loops y sub-workflows), Gmail, Slack y WhatsApp API, API de Claude (lotes, caché de prompts y MCP), agentes con memoria RAG, aprobación humana (HITL) y cuadros de mando. Proyecto final: el sistema de scouting de CS2.<br>
`Make` `n8n` `Airtable` `Gemini` `WhatsApp API` `Claude API` `MCP`

**IA Automation Avanzado** · cursando · [entregas en GitHub](https://github.com/sarlenguito-commits/ia-automation-avanzado)<br>
Agentes autónomos en n8n, arquitectura multi-agente (Manager-Worker, Planner y sub-workflows), guardrails, memoria y persistencia, integraciones con OAuth2 (Gmail, HubSpot y Slack), RAG sobre documentos, voz (bots que escuchan y hablan, con Whisper), agentes por industria, evaluación automática (IA como juez), gobernanza, costos de tokens y observabilidad.<br>
`n8n` `OAuth2` `RAG` `Whisper` `HubSpot` `Slack`

**AI Engineering** · cursando · [primera pre-entrega, aprobada con 91 %](https://github.com/sarlenguito-commits/ia-engineer-1)<br>
Python 3.12 asíncrono, clientes de LLM, cadenas con LangChain, validación estructurada, embeddings y chunking, bases vectoriales (ChromaDB y Pinecone), RAG, agentes con LangGraph (herramientas, ciclos ReAct y checkpoints), sistemas multi-agente con patrón supervisor, observabilidad (Arize Phoenix y LangSmith) y APIs de producción con FastAPI y Redis.<br>
`Python` `LangChain` `LangGraph` `ChromaDB` `Pinecone` `FastAPI`

**🧁 [Poppy Pastelería](https://github.com/sarlenguito-commits/Poppy-Pasteleria-Web-)** · [ver web](https://poppy-pasteleria.netlify.app) · *proyecto final de Desarrollo Web*<br>
Sitio web de repostería artesanal para perros y gatos, hecho para aprender las bases del desarrollo web.<br>
`HTML5` `CSS3` `SCSS` `Grid` `Flexbox` `Bootstrap 5`

---

### 🧰 Herramientas y experiencia

Lo que tengo instalado y uso en mis proyectos y cursos.

**Automatización con IA:** trabajo con **n8n** y **Make** para armar flujos con agentes de IA: leen mails, registran contactos en un CRM, avisan por Slack y dejan borradores para que una persona revise antes de enviar.
**IA y agentes:** `Claude Code` `Codex` `n8n` `Make` `Gemini` `MCP`
**Modelos locales (Ollama):** `Gemma 4` `Qwen 3.5` `DeepSeek R1` `Qwen3 Embedding`
**Voz:** `Whisper` `faster-whisper` (bots que escuchan y hablan)
**APIs y conexiones:** `REST` `Webhooks` `HTTP Request` `OAuth2` `Gmail` `Slack` `HubSpot` `WhatsApp API` `Airtable` `Gemini` `Groq (gpt-oss)` `Claude API`
**Lenguajes:** `JavaScript` `TypeScript` `Python` `HTML` `CSS` `SCSS/Sass` `PowerShell`
**Frontend y escritorio:** `React` `Bootstrap` `Vite` `Electron` `PWA`
**Backend y nube:** `Node.js` `Firebase (Auth + Firestore + Hosting)` `Cloudflare Workers`
**Bases de datos:** `SQLite` `Firestore` `Postgres` `Airtable`
**Pruebas y calidad:** `Vitest` `pruebas automáticas` `emulador de Firebase` `GitHub Actions` `accesibilidad (Axe)`
**Despliegue:** `GitHub Pages` `Firebase Hosting` `Netlify` `Render`
**Herramientas:** `Git/GitHub` `GitHub CLI` `VS Code` `Live Server` `Prettier` `Error Lens` `SQLite Viewer` `REST Client` `Draw.io`
**Estoy aprendiendo:** `LangChain` `LangGraph` `ChromaDB` `Pinecone` `FastAPI` `Redis`
**Probando:** `Docker` y `WSL` (uso experimental), `Laravel` (un trabajo chico para ver cómo funciona) y `Godot` (tengo proyectos de juegos en mente)

---

### 🌱 Primeros proyectos

Mis comienzos en el desarrollo: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([ver web](https://cs2databasetnl.onrender.com)), un CRM de jugadores de CS2 con las APIs de FACEIT y Steam · [🥗 Calculadora Saludable](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)
