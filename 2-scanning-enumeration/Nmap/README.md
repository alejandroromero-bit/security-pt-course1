# Nmap

Nmap (Network Mapper) es **la** herramienta de referencia para descubrir hosts,
puertos y servicios. Su motor de scripts (**NSE**) lo convierte además en un
enumerador y detector de vulnerabilidades muy potente.

Dominar Nmap es imprescindible: casi todo pentest de red empieza aquí.

## 🛠️ Herramientas habituales
`nmap` · scripts `NSE` · `zenmap` (GUI) · salida a `-oN/-oX/-oG`

## 🧪 Ejercicios básicos (individuales)
> Objetivo legal de práctica: **`scanme.nmap.org`**.
> 💻 **Sin VM:** lanza estos escaneos desde [nmap.online](https://nmap.online/) o
> [HackerTarget](https://hackertarget.com/) contra `scanme.nmap.org`.
> Más opciones en [`ONLINE-LABS.md`](../../ONLINE-LABS.md).
1. Descubrimiento de hosts: `nmap -sn scanme.nmap.org`.
2. Servicios y versiones: `nmap -sV scanme.nmap.org`.
3. Enumeración con scripts: `nmap -sC scanme.nmap.org` (scripts "default").

## 👥 Reto colaborativo activo — Utilidades en el día a día

> *"Nmap, Netcat, Nikto y otras utilidades forman parte del día a día en pruebas
> de seguridad."* → Reto actual del curso. Detalles en
> [`ASSIGNMENT-01.md`](../../ASSIGNMENT-01.md).

Haz los ejercicios de arriba **en línea** (ver [`ONLINE-LABS.md`](../../ONLINE-LABS.md)),
en tu propia rama, y documenta tu trabajo en las **tres partes**. Al terminar,
abre un Pull Request (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)). Firma con tu usuario.

### 1. 🎯 Ejercicio
_Herramienta online usada, objetivo (p. ej. `scanme.nmap.org`) y comandos/pasos._

### 2. 📈 Progreso
_Qué fuiste logrando, obstáculos y cómo los resolviste, salidas o capturas clave._

### 3. 📝 Reporte
_Resultados/hallazgos, interpretación, conclusión y próximos pasos._
