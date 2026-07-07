# 🧪 Ejercicios — Escaneo y enumeración

> ⚠️ El objetivo oficial y **legal** para practicar Nmap es
> **`scanme.nmap.org`** (proporcionado por el proyecto Nmap). No escanees IPs
> ajenas sin permiso.

## Ejercicio 1 · Descubrimiento de hosts
**Objetivo:** identificar hosts vivos sin escanear puertos.
1. Ejecuta `nmap -sn scanme.nmap.org`.
2. Explica qué hace el flag `-sn` y por qué es menos intrusivo.

## Ejercicio 2 · Escaneo de puertos y servicios
**Objetivo:** encontrar puertos abiertos y sus versiones.
1. Ejecuta `nmap -sV scanme.nmap.org`.
2. Anota los puertos abiertos, el servicio y la versión detectada.
3. ¿Qué diferencia hay entre un estado `filtered` y `closed`?

## Ejercicio 3 · Enumeración con NSE
**Objetivo:** usar scripts para obtener más detalle.
1. Ejecuta `nmap -sV --script=default scanme.nmap.org`.
2. Investiga qué categoría de scripts es "default" y qué riesgos tiene "intrusive".

## 🏁 Reto
Diseña **un solo comando de Nmap** que: detecte versión, ejecute scripts default,
guarde la salida en formato normal y XML, y use timing moderado. Documenta cada
flag y por qué lo elegiste.
