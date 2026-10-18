### ¡Hola! Soy Esteban 👋

Soy **desarrollador de soluciones de software con IA** y **orquestador de agentes**: diseño qué tiene que resolver cada sistema, coordino a los modelos que lo construyen y verifico que funcione.

Me gusta construir **herramientas que resuelven problemas reales**: apps que hoy usan negocios y personas de verdad, automatizaciones con IA y software de gestión. Soy el fundador de **[Sazzo](https://sazzo.com.ar/)**, donde hago webs, apps y automatizaciones a medida para negocios.

- ✅ Terminé Desarrollo Web en Coderhouse (certificado, 16/10/2026)
- ✅ Terminé IA Automation (nivel inicial) en Coderhouse (certificado, 16/09/2026)
- 🌱 Actualmente: IA Automation Avanzado y AI Engineering
- 📍 Neuquén, Argentina

---

### 🧠 Proyecto principal: Abyss · IA local

*Proyecto personal, en desarrollo · el código va a estar pronto en este perfil*

**Abyss** es mi app para trabajar con **modelos de IA que corren en mi propia PC**, sin nube: elijo qué quiero hacer y Abyss arma el pedido, usa el modelo indicado y controla el resultado. Es donde pongo en práctica lo que estudio: el entorno de trabajo de los agentes (**harness**) y el **desarrollo guiado por especificaciones (SDD)**. Se construye por versiones a partir de una spec aprobada, y las decisiones de diseño se debaten entre dos familias de IA (Claude y Codex) antes de que yo decida.

**Qué hace**
- **5 acciones:** charlar, escribir, revisar, pensar y código. Cada una tiene su **ficha editable** (objetivo, reglas, formato, modelo, contexto, temperatura y si razona), con respaldo e historial.
- **Verificador propio:** revisa las respuestas en vez de confiar en el modelo (por ejemplo, el control del voseo lo decide el verificador, no la IA).
- **Varios modelos locales** (Gemma, Qwen, gpt-oss) con apodos: se eligen y se bajan desde la app, se comparan en un **duelo a ciegas** con votos y "Abyss elige" sugiere cuál usar.
- **Memoria fija** y charlas guardadas en una **base SQLite** con esquema versionado y respaldos.
- **Panel de recursos:** placa de video, RAM y procesador, diciendo siempre qué está **medido**, qué es **estimado** y qué se **desconoce**; al cerrar, libera la placa.
- **Conexión con Claude en los dos sentidos:** un servidor **MCP** deja que los agentes de Claude la consulten y le hagan pedidos (sin poder borrar ni cambiar fichas), y "Mandar a Claude" le pasa una respuesta a una sesión.

**Cómo está hecho**
- Servidor Node cerrado: escucha solo en la PC, rechaza pedidos de otros sitios, usa clave de sesión, límites de tamaño y de cantidad y CSP estricta; lo que responde el modelo se muestra siempre como texto.
- 33 pruebas automáticas con un Ollama falso, y una copia limpia para publicar sin datos personales.
- Diseño propio: paneles plateados y una bestia animada que reacciona.

`Node.js` `SQLite` `Ollama` `MCP` `JavaScript` `SCSS`

---

### 🚀 Lo que hago hoy

**🟢 [Sazzo · demos de software por rubro](https://github.com/sazzo-digital/sazzo-digital.github.io)** · [sazzo.com.ar](https://sazzo.com.ar/) · *mi empresa*<br>
Catálogo con 13 demos de software para negocios (flota, kiosco, canchas, barbería, taller, perfumería, restaurante, contable, librería, ferretería, carnicería, gimnasio e inmobiliaria) que se abren desde un QR y se prueban con un toque, en modo prueba y con datos inventados. Cada demo se puede ver con los colores del negocio. Todas comparten un kit propio, con más de 500 pruebas automáticas y un registro de visitas sin datos personales.<br>
`JavaScript` `SCSS` `Google Apps Script` `GitHub Pages`

**🍽️ Restix** · *software comercial* · [muestra pública](https://github.com/sarlenguito-commits/restix-muestra) · [probarla](https://sarlenguito-commits.github.io/restix-muestra/)<br>
Sistema de gestión para **bares y restaurantes**: programa de escritorio instalable para Windows, con mesas, comandas a cocina, cobro con varios medios de pago y división de cuentas, tres cajas con cierre y arqueo, personal, Pedidos Ya/Delivery, PIN de administrador cifrado, copias de seguridad automáticas y licencias por equipo. La muestra pública corre las mismas pantallas en el navegador, con un bar inventado y pruebas automáticas en GitHub Actions.<br>
`Electron` `React` `TypeScript` `SQLite` `Vite` `Vitest`

**🐾 [Mascota Market · Tareas](https://github.com/sarlenguito-commits/mascota-market)** · [ver app](https://sarlenguito-commits.github.io/mascota-market/) · *en uso real*<br>
App web que usa todos los días el equipo de un pet shop con dos locales: tareas de limpieza por semana y turno, notas de cambio de turno, agenda de la dueña, pedidos a proveedores y de clientes, y notas compartidas (texto o listas para tildar). Datos en tiempo real, login por roles y reglas de seguridad propias.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `GitHub Pages`

**🚚 DGT App · gestión de flota** · *hecha para un cliente, en uso, repositorio privado*<br>
App web para celular que lleva una flota de motos, camionetas y camiones: estado de cada vehículo, choferes por turno con sus recorridos, tareas para choferes y mecánicos, problemas con diagnóstico por tipo, stock de repuestos y avisos. Cuatro roles con permisos propios y más de 400 pruebas automáticas.<br>
`JavaScript` `SCSS` `Firebase Auth` `Firestore` `PWA`

**🤖 [Sistema de Scouting Automatizado — CS2](https://github.com/sarlenguito-commits/sistema-scouting-cs2)**<br>
Ecosistema de automatización con IA (n8n + Airtable + Gemini + WhatsApp) para reclutar jugadores de CS2, con punto de pausa humano (HITL) antes de acciones críticas. Proyecto final del curso de Automatización con IA: aprobado con 72 %.<br>
`n8n` `Airtable` `Gemini` `WhatsApp API`

---

### 🎓 Formación

- [**Desarrollo Web**](./certificado-desarrollo-web.pdf) — Coderhouse (certificado por PedidosYa) — 16/10/2026
- [**AI Automation**](./certificado-ai-automation.pdf) — Coderhouse (certificado por StudioChat) — 16/09/2026

**🧁 [Poppy Pastelería](https://github.com/sarlenguito-commits/Poppy-Pasteleria-Web-)** · [ver web](https://poppy-pasteleria.netlify.app) · *proyecto final de Desarrollo Web*<br>
Sitio web de repostería artesanal para perros y gatos, hecho a mano para aprender las bases del desarrollo web.<br>
`HTML5` `CSS3` `SCSS` `Grid` `Flexbox` `Bootstrap 5`

---

### 🌱 Primeros proyectos

Mis comienzos en el desarrollo: [🎮 CS2database](https://github.com/sarlenguito-commits/CS2database) ([ver web](https://cs2databasetnl.onrender.com)), un CRM de jugadores de CS2 con las APIs de FACEIT y Steam · [🥗 Calculadora Saludable](https://github.com/sarlenguito-commits/calculadora-saludable) · [🎯 FACEIT Premier Checker](https://github.com/sarlenguito-commits/faceit-premier-checker)

---

### 🛠️ Stack

**IA y agentes:** `Claude Code` `Codex` `n8n` `Airtable` `Gemini`
**Frontend:** `HTML` `CSS` `SCSS/Sass` `JavaScript` `TypeScript` `React` `Bootstrap`
**Backend y datos:** `Node.js` `Python` `Firebase (Auth + Firestore)` `Postgres` `SQLite`
**Escritorio:** `Electron`
**Herramientas:** `Git/GitHub` `GitHub Pages` `Render` `Vite`
