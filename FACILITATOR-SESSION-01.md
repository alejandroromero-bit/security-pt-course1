# 👨‍🏫 Guía de instructor — Dinámica colaborativa (30 min)

Bloque práctico de **30 minutos** para insertar en una sesión de 90–120 min.
Los alumnos practican **en línea (sin VM)** y entregan **Ejercicio → Progreso →
Reporte** vía Pull Request. Cubre el [Reto #1](ASSIGNMENT-01.md).

## 🎯 Objetivo
Que cada grupo use una utilidad real del día a día, la ejecute en el navegador y
anote su trabajo. Colaborar en GitHub es un **plus opcional**, no el objetivo.

> 🌱 **Clima de la sesión:** es **exploración, no un examen**. **No se califica.**
> Con principiantes, evita cualquier lenguaje de "evaluación": la meta es que
> prueben, se equivoquen sin miedo y se diviertan. El PR puede esperar.

## 👥 Formación de grupos
Divide la clase en **3 grupos**. Cada grupo toma una estación:

| Grupo | Estación | Herramienta en línea | Objetivo autorizado |
|-------|----------|----------------------|---------------------|
| **A** | Nmap | [nmap.online](https://nmap.online/) o [HackerTarget](https://hackertarget.com/) | `scanme.nmap.org` |
| **B** | Nikto | [HackerTarget Nikto](https://hackertarget.com/nikto-website-scanner/) | `testphp.vulnweb.com` * |
| **C** | Netcat | Terminal en el navegador ([Killercoda](https://killercoda.com/)) | `scanme.nmap.org` |

> \* `testphp.vulnweb.com` es un sitio **deliberadamente vulnerable** publicado por
> Acunetix **para practicar escaneos**. `scanme.nmap.org` es el objetivo oficial de
> práctica de Nmap. **No usar ningún otro objetivo.**

### Roles dentro de cada grupo (rotan si hay tiempo)
- **Operador/a:** ejecuta la herramienta.
- **Escriba:** documenta en el `README.md` de la estación.
- **Relator/a:** presenta el resultado en la puesta en común.

## ⏱️ Cronograma (30 min)
| Min | Actividad |
|-----|-----------|
| 0–5 | Formar grupos, abrir enlaces, repartir roles. Recordar la **regla ética** (solo objetivos autorizados). |
| 5–20 | **Ejercicio en línea** (ver el mini-brief de cada grupo abajo). |
| 20–27 | Anotar **Ejercicio / Progreso / Reporte** (en un borrador). El **PR es opcional** y puede hacerse después, cuando tengan acceso al repo. |
| 27–30 | **Puesta en común:** el relator de cada grupo comparte 1 hallazgo (1 min c/u). |

## 🧭 Mini-briefs por grupo

### Grupo A · Nmap
1. En [nmap.online](https://nmap.online/), lanza un escaneo **Quick Service** a
   `scanme.nmap.org`.
2. Repite con detección de versión (`-sV`) si hay créditos, o usa
   [HackerTarget](https://hackertarget.com/) como alternativa.
3. Anota: puertos abiertos, servicio y versión. Interpreta qué significa cada uno.

### Grupo B · Nikto
1. En [HackerTarget Nikto](https://hackertarget.com/nikto-website-scanner/) escanea
   `testphp.vulnweb.com`.
2. Lista 3 hallazgos y clasifícalos por severidad.
3. Discute cuál verificarían primero y por qué (falsos positivos).

### Grupo C · Netcat
1. Abre un playground Ubuntu en [Killercoda](https://killercoda.com/).
2. **Banner grabbing:** `nc scanme.nmap.org 22` y observa el banner SSH.
3. **Chat/listener** (dos pestañas del terminal): listener `nc -lvnp 4444` en una
   y `nc 127.0.0.1 4444` en la otra; envía texto entre ambas.
4. Explica la diferencia entre listener y cliente.

## 📝 Qué anota cada grupo
En un borrador (o en el `README.md` de su estación si ya tienen acceso), las tres partes:
- **🎯 Ejercicio** — herramienta, objetivo y pasos.
- **📈 Progreso** — obstáculos y cómo los resolvieron, salidas clave.
- **📝 Reporte** — hallazgos, interpretación y conclusión.

> El **PR es opcional** y **no se califica**: si el grupo ya tiene acceso, puede
> subirlo (rama `nmap-grupo-a`, `nikto-grupo-b`, `netcat-grupo-c`); si aún no, se
> deja para después. Lo importante es que hayan practicado.

## ✅ Checklist del instructor
- [ ] Verificar que los enlaces cargan desde la red del aula.
- [ ] Recalcar en voz alta la **regla ética** (solo `scanme.nmap.org` / `testphp.vulnweb.com`).
- [ ] Ir **agregando a los alumnos** como colaboradores *durante* la sesión mientras
      ellos hacen el ejercicio — **no es requisito** para empezar.
- [ ] (Opcional, para después) Proteger `main` cuando empiecen a llegar PRs.

## 🧯 Plan B (si un enlace falla)
- nmap.online sin créditos → usar HackerTarget.
- HackerTarget con límite diario → usar [Pentest-Tools](https://pentest-tools.com/).
- Killercoda lento → usar [Webminal](https://webminal.org/).
