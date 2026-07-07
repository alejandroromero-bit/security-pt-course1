# 8 · Forense y respuesta a incidentes (Forensics & Incident Response)

El lado defensivo: cuando ocurre un incidente, hay que **investigar qué pasó**,
contenerlo y aprender. Este módulo introduce la forense digital y el análisis de
logs, complemento imprescindible de la ofensiva.

## 🎯 Objetivos de aprendizaje
- Conocer las fases de la respuesta a incidentes (IR).
- Preservar evidencia respetando la cadena de custodia.
- Analizar artefactos: memoria, disco y logs.
- Reconstruir una línea de tiempo (timeline) de un ataque.

## 🧠 Conceptos clave
- **Ciclo IR (NIST):** preparación → detección/análisis → contención/erradicación
  → recuperación → lecciones aprendidas.
- **Cadena de custodia:** documentar quién, cuándo y cómo manipuló la evidencia.
- **Volatilidad:** la RAM se pierde al apagar; se recolecta primero.
- **IOC (Indicator of Compromise):** rastro de una intrusión (hash, IP, dominio).
- **Análisis de logs:** correlacionar eventos para detectar comportamiento anómalo.

## 🛠️ Herramientas típicas
`Volatility` · `Autopsy` · `Wireshark` · `Splunk`/`ELK` · utilidades de línea de
comandos (`grep`, `awk`, `jq`)

## 🔗 Recursos
- [Volatility 3 (forense de memoria)](https://github.com/volatilityfoundation/volatility3)
- [Autopsy](https://www.autopsy.com/)
- [SANS DFIR](https://www.sans.org/cyber-security-courses/?focus-area=digital-forensics)
- [MITRE ATT&CK](https://attack.mitre.org/) — para mapear técnicas observadas

👉 Practica con los [ejercicios de este módulo](exercises.md).
