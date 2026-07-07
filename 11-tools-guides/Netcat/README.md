# Netcat

Netcat es la **"navaja suiza" de las redes**: lee y escribe datos sobre conexiones
TCP/UDP. Sirve para transferir archivos, hacer de listener, depurar servicios,
banner grabbing y —en laboratorio— establecer shells. Su versión moderna es
**Ncat** (parte de Nmap), con cifrado y más opciones.

## 🛠️ Herramientas habituales
`nc` (netcat) · `ncat` (Nmap) · `socat` (más avanzado)

## 🧪 Ejercicios básicos (individuales)
> Solo en tu propia máquina o laboratorio.
> 💻 **Sin VM:** practica `nc` en un terminal Linux del navegador como
> [Killercoda](https://killercoda.com/) o [Webminal](https://webminal.org/).
> Ver [`ONLINE-LABS.md`](../../ONLINE-LABS.md).
1. Chat simple entre dos terminales: listener `nc -lvnp 4444` + cliente `nc <ip> 4444`.
2. Transfiere un archivo con `nc` (listener con `>` y cliente con `<`).
3. Banner grabbing: `nc scanme.nmap.org 22` y observa la respuesta.

## 👥 Reto colaborativo activo — Utilidades en el día a día

> *"Nmap, Netcat, Nikto y otras utilidades forman parte del día a día en pruebas
> de seguridad."* → Reto actual del curso. Detalles en
> [`ASSIGNMENT-01.md`](../../ASSIGNMENT-01.md).

Haz los ejercicios de arriba **en línea** (ver [`ONLINE-LABS.md`](../../ONLINE-LABS.md)),
en tu propia rama, y documenta tu trabajo en las **tres partes**. Al terminar,
abre un Pull Request (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)). Firma con tu usuario.

### 1. 🎯 Ejercicio
_Terminal/herramienta online usada, objetivo y comandos/pasos._

### 2. 📈 Progreso
_Qué fuiste logrando, obstáculos y cómo los resolviste, salidas o capturas clave._

### 3. 📝 Reporte
_Resultados/hallazgos, interpretación, conclusión y próximos pasos._
