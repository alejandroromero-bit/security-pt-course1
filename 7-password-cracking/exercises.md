# 🧪 Ejercicios — Cracking de contraseñas

> ⚠️ Crackea **solo hashes que tú generes** o los provistos por un lab. Nunca
> hashes obtenidos de sistemas ajenos.

## Ejercicio 1 · Identificar un hash
**Objetivo:** reconocer el algoritmo.
1. Genera un hash MD5 de una palabra de prueba:
   `echo -n "prueba" | md5sum`.
2. Usa `hashid` (o compara longitud/formato) para identificar el tipo.

## Ejercicio 2 · Ataque por diccionario con John
**Objetivo:** crackear un hash propio.
1. Crea un hash sencillo de una palabra que esté en `rockyou.txt`.
2. Ejecuta `john --wordlist=rockyou.txt hash.txt` y observa el resultado.
3. Explica por qué las contraseñas del diccionario caen al instante.

## Ejercicio 3 · Reglas y mutaciones con Hashcat
**Objetivo:** entender el poder de las reglas.
1. Investiga el modo de reglas de Hashcat (p. ej. `-r rules/best64.rule`).
2. Explica cómo una regla convierte `password` en variantes como `P@ssw0rd!`.

## 🏁 Reto
Compara el tiempo de crackeo de la **misma** contraseña almacenada como MD5 sin
salt vs. bcrypt. Explica por qué las funciones lentas y el salt protegen mejor.
