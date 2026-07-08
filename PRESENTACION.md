# 🧰 Herramientas Esenciales para Pentesting y Ciberseguridad


**Índice:** [Legal](#-1--disclaimer-legal-y-ético) ·
[Ciclo](#-2--el-ciclo-de-pentesting) · [Recon](#-3--reconocimiento-osint-y-dns) ·
[Nmap](#-4--nmap-el-flujo) · [Netcat](#-5--netcat-la-navaja-suiza) ·
[Nikto](#-6--nikto-escáner-web) · [Avanzadas](#-7--herramientas-avanzadas) ·
[Legales](#-8--documentos-legales) · [Reporte](#-9--reporte-profesional) ·
[Labs](#-10--labs-legales-para-practicar) · [Ética](#-11--prácticas-éticas) ·
[Claves](#-12--puntos-clave) · [Recursos](#-13--recursos) ·
[Casos reales](#-14--casos-reales-conocimiento-general)

---

## ⚖️ 1 · Disclaimer legal y ético

Antes de tocar **una sola tecla**, esto es innegociable:

```mermaid
flowchart LR
    A["📄 Autorización escrita"] --> G{"¿Todo en regla?"}
    B["🎯 Scope definido"] --> G
    C["📝 Rules of Engagement"] --> G
    D["🔒 NDA (confidencialidad)"] --> G
    G -- sí --> OK["✅ Puedes iniciar"]
    G -- no --> NO["⛔ Acceso no autorizado = DELITO GRAVE"]
    classDef ok fill:#1a7f37,stroke:#116329,color:#ffffff;
    classDef bad fill:#cf222e,stroke:#a40e26,color:#ffffff;
    class OK ok
    class NO bad
```

✓ Confidencialidad de hallazgos · ✓ No causar daño · ✓ Reportar responsablemente

---

## 🔄 2 · El ciclo de pentesting

```mermaid
flowchart LR
    R["1· RECON<br/>OSINT · DNS · whois (pasivo)"] --> S["2· ESCANEO<br/>Nmap: hosts, puertos"]
    S --> EN["3· ENUMERACIÓN<br/>versiones · banners · NSE"]
    EN --> V["4· BÚSQUEDA DE VULNS<br/>Nikto · Burp · manual"]
    V --> EX["5· EXPLOTACIÓN<br/>PoC · Metasploit (autorizado)"]
    EX --> REP["6· REPORTE<br/>hallazgos · impacto · remediación"]
    REP -. re-test .-> R
    classDef now fill:#1f6feb,stroke:#1158c7,color:#ffffff,stroke-width:2px;
    class S,EN,V now;
```

🔵 **En azul: donde estamos hoy en clase** (Nmap y Nikto).

---

## 🔎 3 · Reconocimiento: OSINT y DNS

> ✓ **Legal siempre** — solo información pública. 🎯 El **70%** del pentesting es
> reconocimiento; menos escaneo activo = menos detección.

```mermaid
flowchart LR
    T["🎯 Objetivo"] --> D["DNS<br/>dig ANY"]
    T --> W["whois<br/>registro del dominio"]
    T --> C["Certificados<br/>crt.sh → subdominios"]
    D & W & C --> P["🗺️ Perfil / superficie de ataque"]
```

```bash
dig scanme.nmap.org ANY
whois scanme.nmap.org
curl -s 'https://crt.sh/?q=%25.target.com&output=json'
```

---

## 📡 4 · NMAP: el flujo

**¿Qué es?** *Network mapper* — la herramienta #1 del pentesting.

```mermaid
flowchart TD
    A["🎯 Objetivo autorizado<br/>scanme.nmap.org"] --> B["Host Discovery<br/>nmap -sn"]
    B --> C{"¿Host vivo?"}
    C -- no --> Z["Siguiente objetivo"]
    C -- sí --> D["Port Scanning<br/>-sS / -sT / -sU"]
    D --> E["Version Detection<br/>-sV"]
    E --> F["NSE Scripts<br/>--script 'default or vuln'"]
    F --> G["📊 Puertos + versiones + posibles CVEs"]
    classDef now fill:#1f6feb,stroke:#1158c7,color:#ffffff,stroke-width:2px;
    class B,D,E,F now;
```

**Host discovery** (ping sweep, ~2-5 s en LAN, ruidoso: ARP/ICMP):
```bash
nmap -sn 192.168.1.0/24
nmap -sn scanme.nmap.org
```
**Port scanning** — 🔵 SYN `-sS` (sigiloso, requiere root) · 🟢 Connect `-sT` (sin
root, más logs) · 🟡 UDP `-sU` (lento). Timing `-T2` (sigilo) → `-T4` (rápido):
```bash
nmap -sS scanme.nmap.org
nmap -sU -p 53,123 scanme.nmap.org
```
**Version + NSE** (buscar CVEs: versión + [cve.mitre.org](https://cve.mitre.org/)):
```bash
nmap -sV scanme.nmap.org
nmap --script "default or vuln" scanme.nmap.org
```
**Escaneo completo (real world, ~15-20 min)** — salida en 3 formatos:
```bash
nmap -A -p- -sV --script "default or vuln" -T3 -oA results scanme.nmap.org
# -A todo · -p- 65535 puertos · -oA results.{nmap,xml,gnmap}
```

---

## 🔧 5 · NETCAT: la navaja suiza

**¿Qué es?** Utilidad universal para TCP/UDP.

```mermaid
flowchart LR
    NC(["🔧 Netcat (nc)"]) --> A["🏴 Banner grabbing<br/>nc -v target 22"]
    NC --> B["🔌 Port scan rápido<br/>nc -zv -w1 target 22 80 443"]
    NC --> C["📡 Listener<br/>nc -l -p 4444"]
    NC --> D["⚠️ Reverse shell (conceptual)<br/>solo autorizado"]
```

```bash
# Banner grabbing
echo -e 'GET / HTTP/1.0\r\n\r\n' | nc target 80
nc -v target 22
# Listener + conexión desde otra terminal
nc -l -p 4444
nc localhost 4444
```
✓ Alternativa moderna: **ncat** (Nmap) o **socat**.

---

## 🕷️ 6 · NIKTO: escáner web

Escaneo **automático** de vulnerabilidades web. ⚠️ Muy ruidoso (lo detectan
IDS/WAF) y con **muchos falsos positivos** → verificar a mano.

```mermaid
flowchart LR
    T["🌐 Web autorizada"] --> N["nikto -h URL"]
    N --> F["Lista de hallazgos"]
    F --> M{"¿Falso positivo?"}
    M -- verificar --> OK["Confirmar manualmente"]
    M -- descartar --> X["Ignorar"]
    OK --> R["📝 Documentar en reporte"]
```

```bash
nikto -h http://target.com -output report.html
nikto -h http://target.com -Tuning 1,2,3   # más selectivo / menos ruidoso
```

---

## 🧩 7 · Herramientas avanzadas

```mermaid
flowchart TB
    P["Pentest"] --> W["🔍 Wireshark<br/>capturar/analizar paquetes"]
    P --> B["🛡️ Burp Suite<br/>proxy interceptor + scanner web"]
    P --> J["🔐 John<br/>cracking offline (diccionario)"]
    P --> M["💣 Metasploit<br/>framework de explotación + payloads"]
```

---

## 📋 8 · Documentos legales

```mermaid
flowchart LR
    ROE["Rules of Engagement<br/>alcance · horarios · contactos"] --> G{"¿Firmado?"}
    NDA["NDA<br/>confidencialidad de datos"] --> G
    AUTH["Certificate of Authorization<br/>firma del cliente · validez"] --> G
    G -- sí --> OK["✅ Adelante"]
    G -- no --> NO["🔴 SIN ESTOS = ILEGAL"]
    classDef bad fill:#cf222e,stroke:#a40e26,color:#ffffff;
    class NO bad
```

---

## 📝 9 · Reporte profesional

```mermaid
flowchart LR
    A["Executive Summary<br/>1-2 págs"] --> B["Methodology<br/>herramientas · fases · límites"]
    B --> C["Detailed Findings<br/>por severidad + PoC"]
    C --> D["Appendix<br/>screenshots · comandos · CVEs"]
```

---

## 🧪 10 · Labs legales para practicar

🟢 **Gratuitos:** [`scanme.nmap.org`](http://scanme.nmap.org) (target oficial Nmap) ·
DVWA (web vulnerable, Docker) · Metasploitable (Linux vulnerable)
🟡 **Freemium:** [TryHackMe](https://tryhackme.com/) · [Hack The Box](https://www.hackthebox.com/)

```mermaid
flowchart LR
    A["CompTIA Security+<br/>mes 1-3"] --> B["CEH<br/>mes 4-6"] --> C["OSCP ⭐<br/>mes 7-12 (la más respetada)"]
```

---

## ✅ 11 · Prácticas éticas

```mermaid
flowchart LR
    E["Ética profesional"] --> S["✅ SIEMPRE"]
    E --> N["⛔ NUNCA"]
    S --> S1["Confidencialidad de hallazgos"]
    S --> S2["No causar daño ni interferencia"]
    S --> S3["Escalada responsable de vulns críticas"]
    N --> N1["Acceder sin autorización (DELITO)"]
    N --> N2["Exfiltrar datos personales"]
    N --> N3["Dejar backdoors o malware"]
    classDef bad fill:#cf222e,stroke:#a40e26,color:#ffffff;
    class N,N1,N2,N3 bad
```

---

## 🎯 12 · Puntos clave

- 🎯 **Nmap** es ~70% del pentesting.
- 🎯 **OSINT** (pasivo) ≈ 60% del reconocimiento.
- 🎯 **Ética y legalidad** son *non-negotiable*.
- 🎯 Un **reporte profesional** = valor real para el cliente.
- 🎯 Certificaciones (**CEH → OSCP**) abren puertas.
- 🎯 Practica **siempre** en labs legales.

---

## 📚 13 · Recursos

📖 [nmap.org/book](https://nmap.org/book/) · [owasp.org](https://owasp.org/) ·
[cve.mitre.org](https://cve.mitre.org/)
🔗 Comunidades: r/cybersecurity · capítulos locales de OWASP · Black Hat / DEF CON
💻 **Next steps:** practica en labs → certifícate (CEH → OSCP) → construye portfolio

---

## 🌍 14 · Casos reales (conocimiento general)

Incidentes **públicos y bien documentados**. El enfoque aquí es **defensivo**: el
mismo reconocimiento y escaneo que un pentester hace **con autorización** revela
justo las exposiciones que estos ataques aprovecharon. Estudiarlos enseña **qué
arreglar**, no cómo atacar.

| Caso (año) | Qué pasó (alto nivel) | Exposición que se aprovechó | 🛡️ Lección defensiva |
|---|---|---|---|
| **WannaCry** (2017) | Ransomware-gusano que se propagó solo por miles de equipos | Servicio **SMB (puerto 445)** sin parchear expuesto en red | Parchear a tiempo, deshabilitar SMBv1, **segmentar** la red |
| **Equifax** (2017) | Brecha de ~147M de registros personales | Componente **web sin parchear** (framework desactualizado) | Inventario de software + **gestión de parches** en apps web |
| **Mirai** (2016) | Botnet de dispositivos IoT usada para ataques masivos | **Telnet (23)** abierto con **credenciales por defecto** | Cambiar credenciales por defecto, **cerrar Telnet**, actualizar IoT |
| **Log4Shell** (2021) | Búsqueda masiva en internet de sistemas vulnerables | Librería **Log4j** vulnerable en apps expuestas | Parcheo urgente, **SBOM** (inventario de dependencias), WAF |
| **Colonial Pipeline** (2021) | Interrupción de infraestructura crítica | Cuenta de **acceso remoto (VPN)** con contraseña filtrada y **sin MFA** | **MFA** en todo acceso remoto, rotación de credenciales, monitoreo |

### Cómo se conecta con lo que vimos hoy

```mermaid
flowchart LR
    S["Escaneo / Enumeración<br/>(Nmap, Netcat)"] --> P1["Puertos y servicios expuestos<br/>SMB 445 · Telnet 23"] --> L1["🛡️ Parchear · cerrar · segmentar"]
    W["Búsqueda de vulns web<br/>(Nikto)"] --> P2["Componentes web sin parchear<br/>frameworks · Log4j"] --> L2["🛡️ Inventario + parcheo (SBOM)"]
    C["Contraseñas<br/>(John · Hashcat)"] --> P3["Credenciales débiles o filtradas<br/>sin MFA"] --> L3["🛡️ MFA + rotación de credenciales"]
    classDef def fill:#1a7f37,stroke:#116329,color:#ffffff;
    class L1,L2,L3 def
```

> 💡 **La idea clave:** la herramienta no es "buena" ni "mala". Un pentester ético
> usa Nmap, Netcat o Nikto para **encontrar y cerrar** estas brechas **antes** que
> un atacante. Ese es el trabajo. 🛡️

---

> **¿Preguntas?** 🙌 Recuerden: **ciberseguridad ofensiva = Ética + Técnica.**
> Para la parte práctica de hoy, ver [`ASSIGNMENT-01.md`](ASSIGNMENT-01.md) y
> [`ONLINE-LABS.md`](ONLINE-LABS.md).
