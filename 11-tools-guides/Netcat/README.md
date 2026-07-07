# Netcat

Netcat es la **"navaja suiza" de las redes**: lee y escribe datos sobre conexiones
TCP/UDP. Sirve para transferir archivos, hacer de listener, depurar servicios,
banner grabbing y —en laboratorio— establecer shells. Su versión moderna es
**Ncat** (parte de Nmap), con cifrado y más opciones.

## 🛠️ Herramientas habituales
`nc` (netcat) · `ncat` (Nmap) · `socat` (más avanzado)

## 🧪 Ejercicios básicos (individuales)
> Solo en tu propia máquina o laboratorio.
1. Chat simple entre dos terminales: listener `nc -lvnp 4444` + cliente `nc <ip> 4444`.
2. Transfiere un archivo con `nc` (listener con `>` y cliente con `<`).
3. Banner grabbing: `nc scanme.nmap.org 22` y observa la respuesta.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Crear una tabla de "recetas" de netcat (transferencia, listener, escaneo).
2. Comparar `nc` vs `ncat` vs `socat`.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade recetas y comandos. Firma con tu usuario._
| Objetivo | Comando | Notas |
|---|---|---|
|  |  |  |
