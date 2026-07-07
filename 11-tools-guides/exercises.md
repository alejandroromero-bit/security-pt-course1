# 🧪 Ejercicios — Herramientas y guías

> ⚠️ Ejecuta todo en **tu propia máquina** o en un laboratorio autorizado.

## Ejercicio 1 · Transferencia de archivos con Netcat
**Objetivo:** entender Netcat como canal.
1. En una máquina: `nc -lvnp 4444 > recibido.txt`.
2. En otra: `nc <IP> 4444 < archivo.txt`.
3. Verifica que el archivo llegó íntegro y explica el flujo.

## Ejercicio 2 · Explorar GTFOBins
**Objetivo:** entender el abuso de binarios legítimos.
1. Busca en [GTFOBins](https://gtfobins.github.io/) un binario común (p. ej. `find`).
2. Explica cómo podría usarse para leer archivos o escalar en un entorno mal configurado.

## Ejercicio 3 · Buscar SUID en Linux
**Objetivo:** reconocer una vía de escalada.
1. En una VM de laboratorio: `find / -perm -4000 -type f 2>/dev/null`.
2. Explica qué es el bit SUID y por qué un binario SUID mal elegido es peligroso.

## 🏁 Reto
Crea tu propio **cheatsheet original** (en Markdown) con los 20 comandos que más
usas, agrupados por tarea. Será tu referencia y material para enseñar a otros.
