# ***⚔️ El Camino del Guerrero Digital***

<p align="center">
  <img src="assets/logo.png" width="350px" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Nivel-Zero_a_Operador-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Enfoque-Ciberseguridad-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Idioma-Español-orange?style=for-the-badge" />
</p>

<p align="center">
  <em>De Zero a Operador en Ciberseguridad</em>
</p>

---

<p align="center">
  <em>Los ordenadores son el campo de batalla del futuro.<br>
  Tú ya tienes lo más difícil: la mentalidad.<br>
  Este es tu camino.</em>
</p>

---

## ***📌 Índice***

<ul>
  <li><a href="#sobre-esta-guia">Sobre esta guía</a></li>
  <li><a href="#equipamiento">Equipamiento del Operador</a></li>
  <li><a href="#fases">Fases del Camino</a>
    <details>
      <summary>Ver fases</summary>
      <ul>
        <li><a href="#fase0">Fase 0 — Preparación del Entorno</a></li>
        <li><a href="#fase1">Fase 1 — Linux + Bash</a></li>
        <li><a href="#fase2">Fase 2 — Python</a></li>
        <li><a href="#fase3">Fase 3 — OSINT y Ciberinteligencia</a></li>
        <li><a href="#fase4">Fase 4 — PHP</a></li>
        <li><a href="#fase5">Fase 5 — JavaScript + PHP</a></li>
        <li><a href="#fase6">Fase 6 — Node.js</a></li>
        <li><a href="#fase7">Fase 7 — Kotlin + Android</a></li>
        <li><a href="#fase8">Fase 8 — C/C++</a></li>
        <li><a href="#fase9">Fase 9 — CTFs</a></li>
      </ul>
    </details>
  </li>
  <li><a href="#informe">Plantilla de Informe de Operaciones</a></li>
  <li><a href="#contacto">Contacto</a></li>
</ul>

---

<div id="sobre-esta-guia"/>

## ***🎯 Sobre esta guía***

Esta guía no es un curso para dummies. No está diseñada para hacértelo fácil. Está diseñada para llevarte desde cero hasta ser un operador técnico en ciberseguridad, paso a paso, con proyectos reales que vas a usar de verdad.

Cada fase tiene tres partes:

- **Por qué importa** — el contexto real en ciberseguridad, para qué se usa en el trabajo
- **Guía paso a paso** — práctica guiada con explicación de cada decisión técnica
- **Informe de operaciones** — documentas lo que construiste con tus propias palabras

Al final del camino no tienes un certificado. Tienes un repositorio de GitHub con proyectos reales y un expediente que habla por ti.

> **Regla de oro con IA:** Puedes usarla para todo. Pero si no puedes explicar lo que generó, no lo entiendes y no vale. El informe de operaciones se escribe siempre con tus propias palabras.

---

<div id="equipamiento"/>

## ***🛠️ Equipamiento del Operador***

Antes de empezar, configura tu entorno de trabajo.

**Control de versiones:**

- **[GitHub](https://github.com)** — cada práctica sube aquí. Tu perfil es tu portfolio. Aprende `git init`, `git add`, `git commit`, `git push` desde el primer día.

**Inteligencia Artificial:**

- **[Claude](https://claude.ai)** — razonamiento técnico denso, código, explicaciones profundas
- **[ChatGPT](https://chatgpt.com)** — dudas rápidas, conceptos generales
- **[GitHub Copilot](https://github.com/features/copilot)** — autocompletado de código dentro del editor

**Documentación continua:**

No documentes cuando acabes. Documenta mientras trabajas.

Cada vez que ejecutas un comando, cada vez que algo falla, cada vez que entiendes por qué funciona algo — lo apuntas. Ese proceso es tu informe de operaciones real. Lo que escribes al final sin notas es una reconstrucción. Lo que escribes mientras trabajas es la verdad.

**Herramientas recomendadas para tomar notas en Markdown:**

| Herramienta | Descripción |
|---|---|
| [Obsidian](https://obsidian.md) | La más potente — notas enlazadas, grafos de conocimiento, plugins, todo local |
| [Joplin](https://joplinapp.org) | Open source, sincronización con la nube, buena para empezar |
| [VS Code](https://code.visualstudio.com) | Preview de Markdown integrado — si ya lo tienes abierto para el código, úsalo también para las notas |

> El flujo es simple: tienes Obsidian o Joplin abierto al lado del editor mientras trabajas. Cada paso que das, cada error que encuentras, cada solución que descubres — lo escribes en ese momento. Cuando acabas la práctica, el informe ya está casi hecho.



| Editor | Uso |
|---|---|
| [VS Code](https://code.visualstudio.com) | Principal — todo excepto Python y Android |
| [PyCharm](https://www.jetbrains.com/pycharm/) | Python |
| [Android Studio](https://developer.android.com/studio) | Kotlin |
| Vim | Obligatorio conocerlo — en servidores Linux no hay alternativa |

---

<div id="fases"/>

## ***⚔️ Fases del Camino***

---

<div id="fase0"/>

## ***🖥️ Fase 0 — Preparación del Entorno***

**Por qué importa:** Un operador no trabaja en su máquina de producción. Aprende a separar entornos desde el primer día.

**Parte 1 — Dual Boot:**
- Instalar Ubuntu junto a Windows en el mismo equipo
- Particionar disco, instalar GRUB, elegir sistema operativo al arrancar
- Recomendado para PCs con pocos recursos donde una VM iría lenta

**Parte 2 — Virtualización:**
- Instalar VMware o VirtualBox sobre tu sistema
- Montar una máquina virtual con Kali Linux o Ubuntu
- Recomendado cuando el equipo tiene recursos suficientes

**Práctica:**
1. Crear una máquina virtual desde cero — configurar RAM, disco, red
2. Instalar el sistema operativo
3. Clonar la máquina virtual — aprenden por qué los snapshots y clones son esenciales: antes de tocar algo crítico, clonas. Si la rompes, restauras en segundos.

**Proyecto:** Máquina virtual funcional con Ubuntu/Kali lista para trabajar + su clon de seguridad.

---

<div id="fase1"/>

## ***🐧 Fase 1 — Linux + Bash***

**Por qué importa:** Linux es el sistema operativo de los servidores, los routers, los dispositivos IoT y la mayoría de infraestructura crítica. Un operador que no maneja Linux no opera.

**Contenido:**
- Navegación del sistema — `ls`, `cd`, `pwd`, `find`, `locate`
- Permisos — `chmod`, `chown`, `sudo`
- Gestión de procesos — `ps`, `top`, `kill`
- Redes — `ifconfig`, `ip`, `netstat`, `ping`, `curl`, `wget`
- Pipes y redirección — `|`, `>`, `>>`, `grep`, `awk`, `sed`
- Gestión de paquetes — `apt`, `dpkg`

**Scripts propuestos:**

| Script | Descripción |
|---|---|
| `sysinfo.sh` | Recoge información del sistema — OS, CPU, RAM, disco, interfaces de red y servicios activos. El primer script de reconocimiento de un operador. |
| `ping_sweep.sh` | Escanea un rango de IPs en la red local con `ping` para detectar hosts activos. Introducción al reconocimiento de red sin herramientas externas. |
| `log_analyzer.sh` | Lee `/var/log/auth.log` y extrae intentos de login fallidos, IPs repetidas y usuarios inexistentes. Primer contacto con análisis de logs reales. |

**Entrega:** Ver sección de [Formatos de Entrega](#entrega).

---

<div id="fase2"/>

## ***🐍 Fase 2 — Python***

**Por qué importa:** Python es el lenguaje de la automatización, el análisis de datos y la ciberseguridad ofensiva y defensiva. La mayoría de herramientas de seguridad están escritas en Python o tienen bindings para él.

**Prácticas:**

| Práctica | Descripción |
|---|---|
| Scripts básicos | Sintaxis, lógica, funciones, ficheros |
| Consumir APIs | GET/POST, JSON, autenticación con API key |
| Telegram Bot | Bot real con BotFather y python-telegram-bot |
| Ollama + FastAPI | Modelo de IA local expuesto como endpoint REST propio |

**Proyecto final:** Bot de Telegram que consulta una API propia montada con FastAPI y un modelo local con Ollama.

---

<div id="fase3"/>

## ***🔍 Fase 3 — OSINT y Ciberinteligencia***

**Por qué importa:** Antes de atacar o defender un sistema, se recopila información. La inteligencia en fuentes abiertas es la primera fase de cualquier operación.

**Herramientas:**

- **[Shodan](https://shodan.io)** — dispositivos expuestos en internet, puertos, banners, versiones
- **[Censys](https://censys.io)** — similar a Shodan, orientado a certificados y servicios
- **[IPInfo](https://ipinfo.io)** — geolocalización, ASN, ownership de IPs
- **[Whois](https://who.is)** — registro de dominios, fechas, propietario
- **[VirusTotal](https://virustotal.com)** — análisis de IPs, dominios, hashes, ficheros
- **[TheHarvester](https://github.com/laramies/theHarvester)** — emails, subdominios y hosts de un dominio objetivo

**Proyecto:** Script Python que dado un dominio o IP consulta varias fuentes automáticamente y genera un informe consolidado en texto.

---

<div id="fase4"/>

## ***🐘 Fase 4 — PHP***

**Por qué importa:** PHP mueve más del 75% de la web. Entender cómo funciona el servidor es entender cómo se explotan la mayoría de vulnerabilidades web — SQLi, LFI, RFI, file upload bypass.

**Contenido:**
- Cómo funciona una petición HTTP desde el lado servidor
- Variables `$_SERVER`, `$_GET`, `$_POST`
- Formularios, ficheros, lógica básica

**Proyecto:** Página web que muestra al visitante todo lo que su navegador filtra sin que lo sepa — IP, User Agent, headers HTTP, idioma, referrer. Lo suben a un hosting gratuito (InfinityFree o Hostinger) y se lo mandan a un compañero.

> Ese momento en el que ven su propia IP en pantalla es el primer momento en que entienden qué significa navegar sin privacidad.

---

<div id="fase5"/>

## ***💬 Fase 5 — JavaScript + PHP***

**Por qué importa:** JavaScript es el lenguaje del navegador. Todo lo que ocurre en el frontend — formularios, peticiones, manipulación del DOM — está escrito en JS. Entenderlo es entender XSS, CSRF y cómo se construyen aplicaciones web reales.

**Contenido:**
- DOM, eventos, `fetch()`, actualización dinámica sin recargar
- Comunicación cliente-servidor
- Backend PHP: recibir, guardar y devolver mensajes

**Proyecto:** Chat web en tiempo real — frontend en JavaScript, backend en PHP. Dos módulos, un producto.

---

<div id="fase6"/>

## ***🟩 Fase 6 — Node.js***

**Por qué importa:** Node.js lleva JavaScript al servidor y a la línea de comandos. Entender que JS no es solo el navegador cambia la perspectiva de cómo funciona la web entera.

**Prácticas:**

| Práctica | Descripción |
|---|---|
| Hola Mundo CLI | JS en terminal, entender el runtime |
| Lector de ficheros | Módulo `fs`, procesamiento de texto |
| Generador de contraseñas | Módulo `crypto`, `process.argv`, herramienta útil real |
| Port Scanner básico | Módulo `net`, conexiones TCP, reconocimiento de red |

**Proyecto final:** Generador de contraseñas por línea de comandos + port scanner básico.

---

<div id="fase7"/>

## ***📱 Fase 7 — Kotlin + Android***

**Por qué importa:** El desarrollo móvil es un paradigma completamente distinto — ciclo de vida de Activities, permisos del sistema operativo, base de datos local. Entender cómo funciona una app móvil es entender cómo se atacan. Kotlin es además el puente natural hacia Java, presente en gran parte de la infraestructura empresarial.

**Contenido:**
- Android Studio, estructura de un proyecto Android
- Activities, ciclo de vida, layouts XML
- Base de datos local con Room/SQLite
- Permisos y gestión de recursos

**Proyecto:** App Android funcional con base de datos local — algo que el alumno decida que va a usar de verdad.

---

<div id="fase8"/>

## ***⚙️ Fase 8 — C/C++***

**Por qué importa:** C y C++ son los lenguajes del sistema operativo, los drivers, el firmware y la mayoría de vulnerabilidades críticas. Entender la gestión manual de memoria es entender por qué existen los buffer overflows, los use-after-free y los exploits de bajo nivel.

**Contenido:**
- Compilación, punteros, gestión manual de memoria
- Stack y heap — cómo se organizan en memoria
- Por qué un buffer overflow ocurre y qué consecuencias tiene

**Referencias:**
- **[cplusplus.com](https://cplusplus.com)** — referencia completa del lenguaje
- **[Cisco NetAcad — C++ Advanced](https://www.netacad.com/es/courses/c-plus-plus-advanced?courseLang=en-US)** — curso estructurado

**Proyecto:** Programa con gestión manual de memoria + demo controlada de buffer overflow para entender el concepto.

---

<div id="fase9"/>

## ***🚩 Fase 9 — CTFs***

**Por qué importa:** Los CTFs son el campo de entrenamiento. Todo lo que aprendiste en las fases anteriores se aplica aquí en escenarios reales y controlados. Es el ejercicio táctico final.

**Plataforma:** [TryHackMe](https://tryhackme.com)

**Path recomendado:**
1. Pre-Security
2. Jr Penetration Tester

**Documentación:** Cada máquina resuelta lleva su writeup — metodología, herramientas usadas, vulnerabilidad explotada, lecciones aprendidas. No vale con resolver. Hay que documentar.

---

<div id="informe"/>

## ***📋 Plantilla de Informe de Operaciones***

Cada práctica completada se documenta con esta estructura:

```
## Informe de Operaciones — [Nombre de la práctica]

**Fase:** 
**Fecha:** 
**Tecnología:** 

### ¿Qué construí?

### ¿Cómo funciona?

### ¿Qué aprendí?

### ¿Qué mejoraría?

### Referencias utilizadas
```

---

<div id="entrega"/>

## ***📦 Formatos de Entrega***

Cada fase puede entregarse en cualquiera de estos formatos — lo importante es que esté documentado y sea tuyo:

**Opción A — Repositorio GitHub** *(recomendado)*
- Un repo por fase con el código, el `README.md` de la práctica y el informe de operaciones
- El historial de commits habla de cómo trabajaste, no solo del resultado final

**Opción B — Documento Markdown**
- Un fichero `.md` con la documentación completa de la fase
- Puede vivir dentro del mismo repositorio GitHub como `INFORME.md`

**Opción C — PDF en LaTeX**
- Documento formal con portada, desarrollo técnico y conclusiones
- Con anexo al repositorio GitHub donde está el proyecto
- Recomendado si quieres algo que puedas presentar o imprimir

> Independientemente del formato elegido, el proyecto de código siempre va en GitHub. El documento es el informe — el repo es la evidencia.

---

<div id="contacto"/>

## ***📬 Contacto***

[![LinkedIn](https://img.shields.io/badge/LinkedIn-María_San_José-0077B5?style=for-the-badge&logo=linkedin)](https://es.linkedin.com/in/mariasanjose)

---

<p align="center">
  <em>El campo de batalla ha cambiado. El guerrero también.</em>
</p>
