# 🧪 Ejercicios — Redes e inalámbricas

> ⚠️ Captura tráfico **solo de tu propia red/equipo**. Interceptar redes ajenas es
> ilegal. Para Wi-Fi, practica únicamente contra tu propio router.

## Ejercicio 1 · Tu primera captura
**Objetivo:** familiarizarte con Wireshark.
1. Captura tráfico de tu interfaz mientras navegas a un sitio HTTP de prueba.
2. Aplica el filtro `http` y localiza una petición `GET`.
3. Identifica IP origen/destino, puerto y cabeceras.

## Ejercicio 2 · Analizar una resolución DNS
**Objetivo:** ver DNS en acción.
1. Filtra por `dns` y provoca una consulta (`nslookup example.com`).
2. Distingue la consulta de la respuesta y anota la IP resuelta.

## Ejercicio 3 · ARP y el riesgo de MITM
**Objetivo:** entender por qué ARP es inseguro.
1. Filtra por `arp` y observa el intercambio `who-has` / `is-at`.
2. Explica en qué consiste el ARP spoofing y cómo se detecta/mitiga.

## 🏁 Reto
Captura el tráfico de un login **HTTP** (en un lab que uses HTTP plano) y demuestra
por qué las credenciales viajan expuestas. Luego explica cómo TLS lo soluciona.
