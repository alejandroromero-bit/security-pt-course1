# 🛡️ Security PDFs Library — Curso de Ethical Hacking para principiantes

Repositorio-curso para introducir a la comunidad al **hacking ético** de forma
estructurada, práctica y legal. Está organizado por **fases de un pentest**, con
teoría, objetivos de aprendizaje, enlaces a las fuentes oficiales y **ejercicios
originales** para practicar en entornos autorizados.

> ⚖️ **Nota importante sobre contenido:** este repositorio **no redistribuye
> material con copyright de terceros**. Solo hospeda documentos de **licencia
> abierta o dominio público** (NIST, CISA, OWASP, CIS, NCSC) y **contenido
> original** escrito para este curso. Para el resto de recursos **enlazamos a la
> fuente original** del autor (ver [`RESOURCES.md`](RESOURCES.md)). Enlazar es
> legal y da crédito a quien lo creó.

## 🎯 A quién va dirigido

A personas que **empiezan** en ciberseguridad ofensiva y quieren una ruta clara.
No se asume experiencia previa más allá de manejo básico de Linux y redes.

## 🧭 Ruta de aprendizaje (12 módulos)

| # | Módulo | Qué aprenderás |
|---|--------|----------------|
| 1 | [Reconocimiento](1-reconnaissance/) | OSINT, enumeración DNS, huella digital de un objetivo |
| 2 | [Escaneo y enumeración](2-scanning-enumeration/) | Nmap, descubrimiento de puertos y servicios |
| 3 | [Análisis de vulnerabilidades](3-vulnerability-assessment/) | Nikto, Burp Suite, escaneo web |
| 4 | [Explotación](4-exploitation/) | Metasploit, generación de payloads |
| 5 | [Seguridad de aplicaciones web](5-web-application-security/) | OWASP Top 10, seguridad de APIs |
| 6 | [Redes e inalámbricas](6-network-wireless/) | Wireshark, pentesting wireless |
| 7 | [Cracking de contraseñas](7-password-cracking/) | John the Ripper, Hashcat |
| 8 | [Forense y respuesta a incidentes](8-forensics-incident/) | Forense digital, análisis de logs |
| 9 | [Certificaciones](9-certifications/) | Rutas hacia CEH y OSCP |
| 10 | [Papers e investigación](10-research-papers/) | Análisis de CVEs |
| 11 | [Herramientas y guías](11-tools-guides/) | Netcat, Linux/Windows |
| 12 | [Misceláneo](12-miscellaneous/) | Frameworks de gobernanza y referencia |

## 📚 Cómo usar este curso

1. Sigue los módulos **en orden** — cada fase se apoya en la anterior.
2. Lee el `README.md` de cada carpeta (teoría + enlaces).
3. Resuelve los ejercicios en `exercises.md` **solo en laboratorios autorizados**.
4. Consulta [`RESOURCES.md`](RESOURCES.md) para profundizar en fuentes originales.

## 👥 Aprendizaje colaborativo (estaciones)

Cada módulo tiene **subcarpetas-estación** (Nmap, OSINT, Burp-Suite, ...) con
explicación, herramientas y ejercicios. Cada estación incluye una sección
**✍️ Aportes del equipo** que los alumnos **completan** trabajando en equipo y
practicando el flujo real de GitHub (rama → commit → Pull Request).

👉 El flujo paso a paso está en [`CONTRIBUTING.md`](CONTRIBUTING.md). Es ideal para
que los participantes **se conozcan, colaboren y aprendan Git** a la vez que el
contenido técnico.

## 🧪 Laboratorios recomendados (legales y gratuitos)

- [TryHackMe](https://tryhackme.com/) — rutas guiadas para principiantes
- [Hack The Box](https://www.hackthebox.com/) y [HTB Academy](https://academy.hackthebox.com/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — gratis
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) — app vulnerable para practicar
- [VulnHub](https://www.vulnhub.com/) — máquinas vulnerables descargables

## ⚠️ Ética y legalidad

El hacking ético **siempre** requiere **autorización explícita y por escrito**
del propietario del sistema. Practicar contra sistemas sin permiso es un delito
en la mayoría de países. Usa únicamente los laboratorios de arriba o entornos
propios. Este curso forma **defensores y profesionales responsables**.

## 📄 Licencia

El **contenido original** de este repositorio (READMEs, ejercicios, índices) se
publica bajo los términos del archivo [`LICENSE`](LICENSE). Los PDFs hospedados
conservan la licencia de sus organizaciones emisoras (NIST, CISA, OWASP, CIS,
NCSC), todas de libre redistribución.
