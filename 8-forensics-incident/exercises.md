# 🧪 Ejercicios — Forense y respuesta a incidentes

> ⚠️ Trabaja con muestras de práctica públicas o datos propios. Nunca con datos
> personales de terceros.

## Ejercicio 1 · Análisis de logs con línea de comandos
**Objetivo:** encontrar actividad sospechosa.
1. Toma un log de acceso web de ejemplo (o genera uno).
2. Con `grep`/`awk`, encuentra: las IPs con más peticiones y los códigos `404`/`401`.
3. Explica qué patrón indicaría un intento de fuerza bruta o de escaneo.

## Ejercicio 2 · Línea de tiempo de un incidente
**Objetivo:** ordenar los hechos.
1. A partir de una serie de eventos de ejemplo, construye una tabla cronológica.
2. Marca el punto probable de compromiso inicial y la propagación.

## Ejercicio 3 · Mapear a MITRE ATT&CK
**Objetivo:** hablar el lenguaje del sector.
1. Elige 3 acciones de un atacante (p. ej. phishing, persistencia, exfiltración).
2. Encuentra la técnica correspondiente en [MITRE ATT&CK](https://attack.mitre.org/).

## 🏁 Reto
Redacta un **informe de incidente** de 1 página: resumen ejecutivo, línea de
tiempo, IOCs, impacto y recomendaciones. Usa el ciclo de IR del NIST como guía.
