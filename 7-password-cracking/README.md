# 7 · Cracking de contraseñas (Password Cracking)

Las contraseñas débiles siguen siendo una de las causas principales de brechas.
Este módulo enseña cómo se **almacenan** (hashes) y cómo se **auditan** con John
the Ripper y Hashcat — siempre sobre hashes propios o de laboratorio.

## 🎯 Objetivos de aprendizaje
- Entender qué es un hash y por qué no se "descifra", se **crackea**.
- Diferenciar ataques por diccionario, por fuerza bruta y con reglas.
- Usar John the Ripper y Hashcat sobre hashes de práctica.
- Comprender el papel del *salt* y de las funciones lentas (bcrypt/argon2).

## 🧠 Conceptos clave
- **Hash:** huella unidireccional de una contraseña (MD5, SHA-256, NTLM, bcrypt).
- **Salt:** valor aleatorio que hace únicos hashes de contraseñas iguales.
- **Ataque por diccionario:** probar palabras de una lista (wordlist).
- **Reglas / mutaciones:** transformar palabras (`p@ssw0rd`) para ampliar cobertura.
- **GPU cracking:** Hashcat aprovecha la GPU para probar millones de hashes/seg.

## 🛠️ Herramientas típicas
`john` (John the Ripper) · `hashcat` · `hashid` · diccionarios (`rockyou`, SecLists)

## 🔗 Recursos
- [John the Ripper](https://www.openwall.com/john/)
- [Hashcat — Wiki](https://hashcat.net/wiki/) · [Hashes de ejemplo](https://hashcat.net/wiki/doku.php?id=example_hashes)
- [SecLists (diccionarios)](https://github.com/danielmiessler/SecLists)

👉 Practica con los [ejercicios de este módulo](exercises.md).
