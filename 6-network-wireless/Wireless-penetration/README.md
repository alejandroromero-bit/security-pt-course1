# Pentesting inalámbrico (Wireless Penetration)

Las redes Wi-Fi añaden una superficie de ataque física: cualquiera dentro del
alcance puede intentar capturar tráfico o atacar la autenticación. Este subtema
cubre los fundamentos de **WPA2/WPA3**, el modo monitor y la captura de handshakes.

> ⚠️ **Solo sobre tu propia red.** Atacar Wi-Fi ajeno es ilegal en casi todos los
> países, incluso "solo por probar".

## 🛠️ Herramientas habituales
`aircrack-ng` (suite) · `airodump-ng` · `wifite` · `kismet` · `hcxdumptool`

## 🧪 Ejercicios básicos (individuales)
> Usa **exclusivamente** tu propio router y adaptador compatible.
1. Investiga cómo poner una tarjeta en **modo monitor**.
2. Explica qué es el *4-way handshake* de WPA2 y por qué su captura permite
   intentar crackeo offline.
3. Compara WPA2 vs WPA3 (SAE) en resistencia a este ataque.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Documentar el flujo teórico: monitor → captura → handshake → crackeo offline.
2. Explicar mitigaciones (contraseñas fuertes, WPA3).
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Documenta conceptos, herramientas y consideraciones legales. Firma con tu usuario._
- Concepto / herramienta:
- Explicación:
- Aprendizaje clave:
