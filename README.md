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

### 🧠 Proyecto destacado: Abyss

*Proyecto personal, en desarrollo · laboratorio local de modelos en una GPU de 8 GB, medido · RAG con mis propios documentos en construcción*

Abyss es el banco de pruebas donde estudio cómo se comportan los modelos de IA locales. Corre en mi PC con Ollama y es 100 % local con el interruptor ONLINE apagado. Es un frontend propio de Ollama, y lo que lo distingue es que **mide y dice qué mide**: cada número es *medido*, *estimado* o *desconocido*, desde los datos hasta la pantalla.

**Lo que ya funciona**
- Acciones de chat (charlar, revisar, pensar, código) con respuesta en vivo y botón de cancelar.
- **Duelos a ciegas** entre modelos: dos respuestas, A y B, con los nombres ocultos hasta que voto. Con 10 o más votos, la recomendación sale de mis votos.
- **Operación en 8 GB:** un pedido por vez, mide cuánta placa ocupa cada modelo, avisa antes si no entra y sugiere uno más chico, y descarga los modelos al cerrar.
- **Memoria gobernada:** lo que genera entra "sin revisar" y solo pasa a su memoria cuando lo apruebo yo.
- **Seguridad de una app local:** solo escucha en mi PC, rechaza pedidos de otros sitios, usa clave de sesión, límites y una política de seguridad estricta, con pruebas.
- **Sin dependencias externas** en ejecución y 60 pruebas automáticas que corren en unos 30 segundos con un Ollama de mentira.

**Los modelos** (Ollama, 18 instalados)
- De uso diario: `gemma4:e4b` (para charlar, unos 84 tokens por segundo), `qwen3.5:4b` (el clasificador que decide qué modelo conviene usar, unos 80), `qwen3.5:9b` (para revisar, unos 56), `deepseek-r1:8b` (para pensar) y `qwen3-embedding:0.6b` (búsqueda por significado, que corre en el procesador).
- Grandes, probados en la misma placa: `gpt-oss:20b`, `gemma4:26b` y `qwen3.6:35b`. No entran enteros en 8 GB y van entre 19 y 28 tokens por segundo.
- Las velocidades las medí en octubre con otra versión de Ollama; las voy a volver a medir.

**Lo que viene:** un RAG con mis propios documentos que corra local: cargarlos y trocearlos, citar la fuente y responder "no sé" cuando no hay dato, con un plan de medición definido antes de construir (30 a 50 preguntas, con un grupo reservado). Hoy lo que existe es la búsqueda por significado de notas cortas, no un RAG completo.<br>
`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

<details>
<summary>🔧 Cómo vive Abyss por dentro</summary>

- **Arranque:** un acceso directo abre Ollama si está cerrado, levanta un servidor Node oculto y abre Abyss en una ventana propia del navegador. Al cerrar la ventana, el servidor se apaga solo y descarga los modelos que usó.
- **Servidor:** Node.js puro, sin librerías externas ni `package.json` (solo módulos propios de Node, con SQLite integrado). Escucha únicamente en mi PC, rechaza pedidos de otros sitios, usa una clave de sesión distinta en cada arranque, límites de tamaño y de cantidad y una política de seguridad estricta. Lo que responde el modelo se muestra como texto o escapado, nunca como HTML.
- **Conexión con Ollama:** el servidor le habla por su API local: lista los modelos instalados, ve cuál está cargado en la placa, pide las respuestas en vivo (streaming), genera las huellas (embeddings) en el procesador y carga y descarga modelos con el contexto de cada ficha. Baja modelos nuevos solo de una lista fija y con un clic.
- **ONLINE / OFFLINE:** arranca apagado. Prendido, sale a Wikipedia, Wikidata, el clima, los feriados, los links que pego y un metabuscador propio (SearXNG, en Docker) que reenvía la consulta a buscadores de internet; sale solo la consulta. Apagado, usa lo guardado y una Wikipedia local (Kiwix, en Docker), una copia de octubre.
- **Del modelo a la pantalla:** el servidor reenvía lo que va generando el modelo en un flujo continuo y la ventana lo pinta a medida que llega.
- **Front:** HTML, JavaScript por módulos sin frameworks y SCSS compilado a un solo archivo de estilos. Modo consola (ventanas negras translúcidas) y una bestia animada que reacciona.
- **Fichas:** cada acción tiene su ficha editable (objetivo, reglas, formato, modelo, contexto, temperatura y tope de tokens), con la versión anterior guardada, y con ella el servidor arma el pedido a Ollama. Un verificador revisa el voseo.
- **Medición:** lee la placa, la RAM y el procesador, y cada número dice si es medido, estimado o desconocido. Cuánto ocupa cada modelo se mide la primera vez; "entra / no entra" es una estimación.
- **Datos:** una base SQLite con esquema versionado y respaldos completos que se verifican al restaurar.
- **Conexión con Claude:** un servidor MCP con 5 herramientas deja que los agentes de Claude le hagan pedidos, sin poder borrar, cambiar fichas ni aceptar propuestas.
- **Cómo se construyó:** con agentes de IA (Claude Code y Codex) a partir de una especificación que yo apruebo, por versiones, con 60 pruebas automáticas.

</details>

---

### 🚀 Lo que hago hoy

En uso real hoy: **Mascota Market** (el equipo de un pet shop) y **DGT App** (la flota de un cliente). **Restix** es un producto propio en desarrollo. También automatizo procesos con agentes de IA en **n8n**.

**🍽️ Restix** · *producto propio, en desarrollo* · [muestra pública](https://github.com/sarlenguito-commits/restix-muestra) · [probarla](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Sistema de gestión para **bares y restaurantes**: programa de escritorio instalable para Windows, con mesas, comandas a cocina, cobro con varios medios de pago y división de cuentas, tres cajas con cierre y arqueo, personal, ventas por canal (salón y Pedidos Ya/Delivery), PIN de administrador protegido, copias de seguridad automáticas y licencias por equipo. La muestra pública corre las mismas pantallas en el navegador, con un bar inventado y pruebas automáticas en GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tareas](https://github.com/sarlenguito-commits/mascota-market)** · [ver app](https://sarlenguito-commits.github.io/mascota-market/) · *en uso real*<br>
App web que usa el equipo de un pet shop con dos locales: tareas de limpieza por semana y turno, notas de cambio de turno, agenda de la dueña, pedidos a proveedores y de clientes, y notas compartidas (texto o listas para tildar). Datos en tiempo real, login por roles y reglas de seguridad propias.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · gestión de flota** · *hecha para un cliente, en uso, repositorio privado*<br>
App web para celular que lleva una flota de motos, camionetas y camiones: estado de cada vehículo, choferes por turno con sus recorridos, tareas para choferes y mecánicos, problemas con diagnóstico por tipo, stock de repuestos y avisos. Cinco roles con permisos propios y más de 3.000 pruebas automáticas: la lógica sin conexión, las pantallas en el navegador y las reglas de seguridad contra un emulador de Firebase.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Sistema de Scouting Automatizado — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
Ecosistema de automatización con IA (n8n + Airtable + Gemini + WhatsApp) para reclutar jugadores de CS2, con punto de pausa humano (HITL) antes de acciones críticas. Proyecto final del curso de Automatización con IA: aprobado con 72 %.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

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

**Lo que viene:** llevar este trabajo a modelos locales en Abyss, con la especificación y el plan de medición escritos antes de construir.

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
**Probando:** `Docker` (lo uso en Abyss para la Wikipedia local y el buscador propio) y `WSL` (uso experimental), `Laravel` (un trabajo chico para ver cómo funciona) y `Godot` (tengo proyectos de juegos en mente)

---

### 🌱 Primeros proyectos

Mis comienzos en el desarrollo: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([ver web](https://cs2databasetnl.onrender.com)), un CRM de jugadores de CS2 con las APIs de FACEIT y Steam · [🥗 Calculadora Saludable](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)
