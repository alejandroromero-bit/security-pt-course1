# 1 · Reconocimiento (Reconnaissance)

El reconocimiento es la **primera fase** de todo pentest: recopilar información
sobre el objetivo **antes** de interactuar de forma intrusiva. Cuanto mejor sea
tu reconocimiento, más eficaces serán las fases siguientes.

## 🎯 Objetivos de aprendizaje
- Distinguir reconocimiento **pasivo** (sin tocar el objetivo) de **activo**.
- Recopilar información pública con técnicas **OSINT**.
- Enumerar registros **DNS** y descubrir subdominios.
- Construir la "huella digital" (footprint) de una organización.

## 🧠 Conceptos clave
- **OSINT (Open Source Intelligence):** inteligencia a partir de fuentes públicas
  (webs, redes sociales, registros WHOIS, certificados, filtraciones).
- **Reconocimiento pasivo:** no generas tráfico hacia el objetivo (Google, WHOIS,
  crt.sh). Difícil de detectar.
- **Reconocimiento activo:** consultas directas (resolución DNS, banners). Más
  información, pero deja rastro.
- **Superficie de ataque:** conjunto de puntos expuestos (dominios, IPs, correos,
  tecnologías) por donde se podría atacar.

## 🛠️ Herramientas típicas
`whois` · `dig` / `nslookup` · `theHarvester` · `amass` · `dnsdumpster` · `crt.sh`
· buscadores (Google dorks) · `Shodan`

## 🔗 Recursos
- [OSINT Framework](https://osintframework.com/)
- [MITRE ATT&CK — Reconnaissance](https://attack.mitre.org/tactics/TA0043/)
- [theHarvester](https://github.com/laramies/theHarvester) · [OWASP Amass](https://github.com/owasp-amass/amass)
- [crt.sh](https://crt.sh/) · [DNSDumpster](https://dnsdumpster.com/)

👉 Practica con los [ejercicios de este módulo](exercises.md).
