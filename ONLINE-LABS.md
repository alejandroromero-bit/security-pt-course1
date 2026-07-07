# 🌐 Laboratorios y herramientas EN LÍNEA (sin montar máquina virtual)

Estos recursos permiten practicar **desde el navegador**, sin instalar nada ni
montar una VM. Ideales para las primeras sesiones del curso.

> ⚠️ **Regla ética innegociable:** los escáneres en línea (nmap.online,
> HackerTarget, pentest-tools…) pueden apuntar a **cualquier** objetivo que
> escribas. **Solo** escanea sistemas **propios** o de práctica autorizada. El
> objetivo legal por defecto para Nmap es **`scanme.nmap.org`**. Escanear a
> terceros sin permiso es delito, aunque sea "solo por probar".

## 🖥️ Terminales y entornos completos en el navegador
Para practicar comandos reales (`nmap`, `nc`, `nikto`, Linux) sin instalar:
- **[Killercoda](https://killercoda.com/)** — escenarios interactivos con terminal
  Linux en el navegador. Gratis.
- **[Webminal](https://webminal.org/)** — terminal Linux online con lecciones
  guiadas. Gratis (requiere registro).
- **[TryHackMe](https://tryhackme.com/)** — su **AttackBox** es un Kali completo en
  el navegador; muchas salas para principiantes. Gratis con límites de tiempo.
- **[OverTheWire — Bandit](https://overthewire.org/wargames/bandit/)** — aprende
  línea de comandos y SSH resolviendo niveles. Gratis.

## 📡 Escaneo de red y puertos (módulos 1–2)
- **[nmap.online](https://nmap.online/)** — Nmap desde el navegador (versión, OS,
  timing). Gratis con límite de créditos.
- **[HackerTarget](https://hackertarget.com/)** — Nmap online, DNS lookup, whois,
  traceroute, reverse IP, geolocalización… Gratis con límite diario de consultas.
- **[Pentest-Tools](https://pentest-tools.com/)** — Port/Network Scanner,
  Subdomain Finder, URL Fuzzer. Versión "light" gratis.

## 🔎 Reconocimiento / OSINT (módulo 1)
- **[DNSDumpster](https://dnsdumpster.com/)** — mapa DNS y subdominios.
- **[crt.sh](https://crt.sh/)** — subdominios vía Certificate Transparency.
- **[ViewDNS.info](https://viewdns.info/)** — colección de herramientas DNS/red.
- **[Shodan](https://www.shodan.io/)** — buscador de dispositivos expuestos (registro).

## 🐞 Escaneo web y vulnerabilidades (módulo 3)
- **[HackerTarget — Nikto](https://hackertarget.com/nikto-website-scanner/)** —
  escáner Nikto en línea. Gratis con límite.
- **[Pentest-Tools — Website Scanner](https://pentest-tools.com/website-vulnerability-scanning/website-scanner)** — escáner web (light gratis).
- **[Qualys SSL Labs](https://www.ssllabs.com/ssltest/)** — análisis TLS/SSL de un sitio.
- **[urlscan.io](https://urlscan.io/)** — analiza qué hace una URL.

## 🌐 Aplicaciones web para hackear (módulo 5)
Apps **deliberadamente vulnerables**, muchas jugables online:
- **[PortSwigger Web Security Academy](https://portswigger.net/web-security)** —
  labs en el navegador (gratis, requiere cuenta). **El mejor punto de partida web.**
- **[OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)** — hay demo
  online enlazada en la página del proyecto.
- **[Google Gruyere](https://google-gruyere.appspot.com/)** — app vulnerable para aprender.
- **[Root Me](https://www.root-me.org/)** — retos de seguridad online por categorías.

## 🔑 Cracking e identificación de hashes (módulo 7)
- **[CrackStation](https://crackstation.net/)** — crackeo por tablas (solo hashes propios/prueba).
- **[Hashes.com](https://hashes.com/en/tools/hash_identifier)** — identificar tipo de hash.

## 📄 Análisis de CVEs (módulo 10)
- **[NVD](https://nvd.nist.gov/)** · **[CVE.org](https://www.cve.org/)** ·
  **[CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)** ·
  **[Exploit-DB](https://www.exploit-db.com/)**

---

### 🧭 Recomendación de uso para el curso
1. **Sesiones 1–2:** terminal en el navegador (Killercoda/Webminal) para comandos
   básicos + escáneres online (nmap.online, HackerTarget) contra `scanme.nmap.org`.
2. **Web:** PortSwigger Academy (imbatible y gratis).
3. Cuando el grupo esté listo, dar el salto a **TryHackMe** (AttackBox) para un
   entorno más realista, siempre en el navegador.
