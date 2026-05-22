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
        <li><a href="#fase7">Fase 7 — Docker</a></li>
        <li><a href="#fase8">Fase 8 — Kotlin + Android</a></li>
        <li><a href="#fase9">Fase 9 — C/C++</a></li>
        <li><a href="#fase10">Fase 10 — CTFs</a></li>
      </ul>
    </details>
  </li>
  <li><a href="#recursos">Recursos Recomendados</a></li>
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

## ***🐳 Fase 7 — Docker***

**Por qué importa:** Docker es el estándar de la industria para desplegar aplicaciones. En ciberseguridad lo encontrarás en laboratorios, en infraestructura de CTFs, en entornos de análisis de malware y en cualquier empresa. Entender contenedores es entender cómo se aíslan procesos, redes y sistemas de ficheros — conceptos directamente aplicables a seguridad.

**Contenido:**
- Diferencia entre imagen y contenedor
- `Dockerfile` — construir tu propia imagen
- `docker-compose` — orquestar múltiples contenedores
- Redes en Docker — cómo se comunican los contenedores entre sí
- Volúmenes — persistencia de datos

**Proyecto:** Dockerizar el servidor FastAPI + Ollama construido en la Fase 2. Lo que antes requería configuración manual ahora arranca con un `docker-compose up`. Entienden por qué eso cambia todo.

---

<div id="fase8"/>

## ***📱 Fase 8 — Kotlin + Android***

**Por qué importa:** El desarrollo móvil es un paradigma completamente distinto — ciclo de vida de Activities, permisos del sistema operativo, base de datos local. Entender cómo funciona una app Android por dentro es entender cómo funciona el malware móvil por dentro. Si lo has construido, lo reconoces cuando lo analizas.

**Práctica 1 — App básica:**
- Android Studio, estructura de un proyecto Android
- Activities, ciclo de vida, layouts XML
- Base de datos local con Room/SQLite
- Permisos y gestión de recursos

**Práctica 2 — Servicio en background + alarmas:**
- Crear un `Service` sin interfaz — una aplicación que corre invisible en segundo plano
- `AlarmManager` para programar tareas periódicas
- `BroadcastReceiver` para reaccionar a eventos del sistema
- Por qué importa: la persistencia y la ejecución silenciosa son los pilares del malware móvil

**Práctica 3 — Recolección de datos y envío a servidor:**
- Recoger información del dispositivo — localización, contactos, logs
- Enviar los datos a un servidor propio vía HTTP (el servidor PHP o FastAPI que ya construyeron)
- Por qué importa: cuando analices una app maliciosa haciendo exfiltración de datos, sabrás exactamente qué está ocurriendo y cómo detectarlo

> Estas tres prácticas no enseñan a crear malware. Enseñan a entenderlo. Un analista que ha construido un servicio en background y una rutina de exfiltración reconoce esos patrones en cualquier APK que le pongan delante.

---

<div id="fase9"/>

## ***⚙️ Fase 9 — C/C++***

**Por qué importa:** C y C++ son los lenguajes del sistema operativo, los drivers, el firmware y la mayoría de vulnerabilidades críticas. Pero en este contexto hay algo igual de importante: la mayoría del malware sofisticado está escrito en C/C++. Si entiendes el lenguaje, entiendes el malware.

**Referencias:**
- **[cplusplus.com](https://cplusplus.com)** — referencia completa del lenguaje
- **[Cisco NetAcad — C++ Advanced](https://www.netacad.com/es/courses/c-plus-plus-advanced?courseLang=en-US)** — curso estructurado

**Práctica 1 — Aplicación con interfaz: captura de pantalla:**
- Aplicación con ventana que captura la pantalla con `GDI+` (`BitBlt`, `GetDC`) y guarda los screenshots en una carpeta
- Por qué importa: los screenshots **requieren contexto de usuario** — acceso al escritorio, a la sesión activa. No se pueden hacer desde un servicio. Cuando analizan malware que hace screenshots, saben exactamente por qué ese malware necesita ejecutarse en contexto de usuario y no como servicio de sistema.

**Práctica 2 — Servicio de Windows con reverse shell:**
- Crear un servicio de Windows real — sin interfaz, corriendo en background bajo el sistema
- El servicio abre una conexión TCP saliente y entrega una shell remota
- Por qué importa: la reverse shell es el mecanismo de control remoto más común en malware. Haberla construido desde cero significa entender cada byte de lo que ves en un análisis de tráfico o en un desensamblado.

> Quien ha construido estas dos piezas reconoce los patrones en cualquier muestra que analice.

---

<div id="fase10"/>

## ***🚩 Fase 10 — CTFs***

**Por qué importa:** Los CTFs son el campo de entrenamiento. Todo lo que aprendiste en las fases anteriores se aplica aquí en escenarios reales y controlados. Es el ejercicio táctico final.

**Plataforma:** [TryHackMe](https://tryhackme.com)

---

**Path 1 — Pre-Security**

Fundamentos técnicos antes de tocar nada ofensivo. Cubre:

- **Redes** — modelo OSI, TCP/IP, DNS, HTTP, cómo viaja un paquete de A a B. Complemento directo a lo visto con Wireshark
- **Sistemas operativos** — Linux y Windows desde el punto de vista de la seguridad, permisos, procesos, ficheros de sistema
- **Fundamentos web** — cómo funciona una petición HTTP, cookies, sesiones, cabeceras. Conecta con las prácticas de PHP y JavaScript

---

**Path 2 — Jr Penetration Tester**

El núcleo del camino. Cubre en orden:

- **OSINT** — recopilación de información en fuentes abiertas, Google Dorks, Shodan, Maltego. Conecta directamente con la Fase 3
- **Redes con Wireshark** — captura y análisis de tráfico, filtros, identificación de protocolos, extracción de credenciales en claro y ficheros de capturas `.pcap`
- **Hashes y CyberChef** — identificación de tipos de hash, operaciones de encoding/decoding, análisis forense básico de datos. CyberChef como navaja suiza del analista
- **Esteganografía** — datos ocultos en imágenes y ficheros de audio, herramientas como `steghide`, `exiftool`, `binwalk`. Muy presente en CTFs
- **Ataques al prompt de IA** — prompt injection, jailbreaking, manipulación de modelos de lenguaje como vector de ataque emergente
- **Explotación web** — SQLi, XSS, IDOR, file upload bypass, LFI/RFI
- **Privilege escalation** — Linux y Windows, SUID, servicios mal configurados, tokens de acceso
- **Metasploit** — framework de explotación, módulos, payloads, sessions

---

**Documentación:** Cada máquina resuelta lleva su writeup — metodología, herramientas usadas, vulnerabilidad explotada, lecciones aprendidas. No vale con resolver. Hay que documentar.

---

<div id="recursos"/>

## ***📚 Recursos Recomendados***

Materiales de referencia para complementar cada fase del camino. Gratuitos o con versión gratuita suficiente para empezar.

**Programación general:**
- **[MoureDev — Cursos](https://moure.dev/cursos)** — Brais Moure. Cursos de programación en español de altísima calidad. Python, Kotlin, Git y más. El referente en castellano.
- **[W3Schools](https://www.w3schools.com)** — Referencia rápida para HTML, CSS, JavaScript, PHP, Python y SQL. Ideal para consultar sintaxis mientras programas.
- **[Luis Llamas — Cursos](https://www.luisllamas.es/cursos/)** — Electrónica, programación, IoT y automatización. Muy útil para entender cómo el software interactúa con el hardware.
- **[Píndoras informáticas](https://www.pildorasinformaticas.es/)** — Cursos gratuitos y de pago de programación.

**Python:**
- **[Harvard CS50P — Introduction to Programming with Python](https://pll.harvard.edu/course/cs50s-introduction-programming-python)** — El curso introductorio de Python de Harvard. Gratuito, riguroso y con certificado.

**C/C++:**
- **[cplusplus.com](https://cplusplus.com)** — Referencia completa del lenguaje con ejemplos.
- **[cppreference.com](https://cppreference.com)** — La referencia técnica definitiva de C y C++.
- **[Microsoft Learn — C++](https://learn.microsoft.com/es-es/cpp/cpp/)** — Documentación oficial de Microsoft, muy bien estructurada.
- **[Cisco NetAcad — C++ Advanced](https://www.netacad.com/es/courses/c-plus-plus-advanced?courseLang=en-US)** — Curso estructurado gratuito.

**Kotlin + Android:**
- **[Android Developers — Guía oficial](https://developer.android.com/guide)** — Documentación oficial de Google para desarrollo Android.
- **[Kotlin — Documentación oficial](https://kotlinlang.org/docs/home.html)** — Referencia completa del lenguaje por JetBrains.
- **[Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course)** — Curso gratuito oficial de Google para aprender Android desde cero.

**JavaScript / Web:**
- **[MDN Web Docs](https://developer.mozilla.org/es/)** — La biblia de JavaScript, HTML y CSS. Mozilla. Gratuito y en español.

**Docker:**
- **[Docker Docs](https://docs.docker.com)** — Documentación oficial con tutoriales de inicio muy accesibles.

**Linux + Bash:**
- **[OverTheWire — Bandit](https://overthewire.org/wargames/bandit/)** — Wargame gratuito para aprender Linux y bash resolviendo retos. Complemento perfecto para la Fase 1.

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
