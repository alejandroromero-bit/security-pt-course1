# John the Ripper

John the Ripper (JtR) es un **crackeador de contraseñas** clásico y muy flexible.
Detecta automáticamente muchos formatos de hash y combina ataques por diccionario,
reglas y fuerza bruta. Ideal para aprender los fundamentos antes de pasar a la GPU
con Hashcat.

## 🛠️ Herramientas habituales
`john` · utilidades `unshadow`, `zip2john`, `ssh2john` · diccionarios (`rockyou`, SecLists)

## 🧪 Ejercicios básicos (individuales)
> Crackea **solo hashes que tú generes**.
1. Genera un hash propio y crackéalo:
   `john --wordlist=rockyou.txt hash.txt`.
2. Usa `unshadow` (en un lab) para combinar `passwd` + `shadow`.
3. Prueba el modo `--rules` y explica qué aporta.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Documentar los utilitarios `*2john` y para qué sirven.
2. Comparar modo diccionario vs. incremental.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade comandos, formatos y tiempos. Firma con tu usuario._
- Comando:
- Tipo de hash / resultado:
- Aprendizaje clave:
