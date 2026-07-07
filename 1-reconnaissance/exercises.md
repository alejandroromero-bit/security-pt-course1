# 🧪 Ejercicios — Reconocimiento

> ⚠️ Usa **solo** dominios propios o de práctica autorizada
> (`example.com`, `scanme.nmap.org`, tu propio dominio). Nunca objetivos reales
> sin permiso escrito.

## Ejercicio 1 · WHOIS y huella básica
**Objetivo:** obtener datos de registro de un dominio.
1. Ejecuta `whois example.com`.
2. Identifica: registrador, fechas de creación/expiración y servidores DNS.
3. Anota qué información sería útil para un atacante y por qué.

## Ejercicio 2 · Enumeración DNS
**Objetivo:** descubrir registros DNS de un dominio.
1. Usa `dig` para consultar registros `A`, `MX`, `NS` y `TXT`:
   `dig example.com ANY` (o consulta cada tipo por separado).
2. Explica para qué sirve cada tipo de registro.
3. ¿Qué registro `TXT` suele revelar el proveedor de correo o SPF?

## Ejercicio 3 · Subdominios vía Certificate Transparency
**Objetivo:** encontrar subdominios sin tocar el objetivo (100% pasivo).
1. Entra en [crt.sh](https://crt.sh/) y busca `%.tu-dominio.com`.
2. Lista los subdominios que aparezcan en certificados emitidos.
3. Reflexiona: ¿por qué esta técnica es difícil de detectar?

## 🏁 Reto
Elabora un **informe de reconocimiento de 1 página** de un dominio de práctica:
dominios/subdominios encontrados, tecnologías detectadas y superficie de ataque
estimada. Estructúralo como lo haría un pentester profesional.
