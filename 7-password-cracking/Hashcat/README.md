# Hashcat

Hashcat es el crackeador de contraseñas **acelerado por GPU** más rápido. Gracias
a sus **reglas** y **máscaras** puede probar miles de millones de candidatos por
segundo, por lo que demuestra de forma contundente por qué las contraseñas cortas
o predecibles son inseguras.

## 🛠️ Herramientas habituales
`hashcat` · `hashid` (identificar) · reglas (`rules/best64.rule`) · máscaras (`?a?a?a...`)

## 🧪 Ejercicios básicos (individuales)
> Solo hashes propios o de laboratorio.
1. Identifica un hash con `hashid` y localiza su modo (`-m`) en la
   [tabla de ejemplos](https://hashcat.net/wiki/doku.php?id=example_hashes).
2. Lanza un ataque por diccionario: `hashcat -m 0 hash.txt rockyou.txt`.
3. Añade reglas (`-r rules/best64.rule`) y compara resultados.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Explicar los **modos de ataque** (diccionario, combinación, máscara, híbrido).
2. Documentar cómo se construye una máscara.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade modos, máscaras y tiempos. Firma con tu usuario._
- Modo / comando:
- Resultado:
- Aprendizaje clave:
