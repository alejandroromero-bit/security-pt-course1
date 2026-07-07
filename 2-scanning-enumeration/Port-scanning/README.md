# Escaneo de puertos (Port Scanning)

El escaneo de puertos determina **qué servicios están accesibles** en un host.
Entender los tipos de escaneo (SYN, connect, UDP) y los estados de puerto
(`open`, `closed`, `filtered`) es clave para interpretar resultados sin sacar
conclusiones erróneas.

## 🛠️ Herramientas habituales
`nmap` · `masscan` (muy rápido) · `rustscan` · `netcat` · `unicornscan`

## 🧪 Ejercicios básicos (individuales)
> 💻 **Sin VM:** usa [nmap.online](https://nmap.online/) o
> [Pentest-Tools Port Scanner](https://pentest-tools.com/) contra `scanme.nmap.org`.
> Ver [`ONLINE-LABS.md`](../../ONLINE-LABS.md).
1. Escanea los 1000 puertos más comunes de `scanme.nmap.org` y anota los abiertos.
2. Compara un escaneo TCP (`-sT`) con uno UDP (`-sU`) y explica por qué el UDP es
   más lento y menos fiable.
3. Investiga la diferencia práctica entre `closed` y `filtered`.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Explicar en la sección de abajo los estados de puerto con ejemplos.
2. Comparar velocidad/ruido de `masscan` vs. `nmap`.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Documenta estados de puerto, herramientas y hallazgos. Firma con tu usuario._
- Herramienta / comando:
- Observación:
- Aprendizaje clave:
