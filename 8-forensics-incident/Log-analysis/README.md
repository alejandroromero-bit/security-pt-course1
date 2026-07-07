# Análisis de logs (Log Analysis)

Los logs son la memoria de un sistema. Analizarlos permite **detectar ataques**,
reconstruir su cronología y generar indicadores de compromiso. Va desde comandos
simples (`grep`, `awk`) hasta plataformas SIEM (Splunk, ELK).

## 🛠️ Herramientas habituales
`grep` / `awk` / `cut` / `sort` · `jq` (JSON) · `Splunk` · `ELK` (Elastic) ·
reglas `Sigma`

## 🧪 Ejercicios básicos (individuales)
1. En un log de acceso web de ejemplo, halla las IPs con más peticiones (`awk`+`sort`).
2. Filtra códigos `401`/`403` y explica qué patrón sugiere fuerza bruta.
3. Investiga qué es una regla **Sigma** y para qué sirve.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Crear una "chuleta" de comandos para triaje de logs.
2. Documentar 3 patrones de ataque visibles en logs.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade comandos, patrones e IOCs. Firma con tu usuario._
- Comando / consulta:
- Qué detecta:
- Aprendizaje clave:
