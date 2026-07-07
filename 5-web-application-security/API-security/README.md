# Seguridad de APIs (API Security)

Las APIs son el pegamento de las apps modernas y tienen **riesgos propios**
distintos de las webs tradicionales. OWASP mantiene un **API Security Top 10**
específico. Fallos típicos: autorización a nivel de objeto rota (**BOLA/IDOR**),
exposición excesiva de datos y falta de límites de tasa.

## 🛠️ Herramientas habituales
`Postman` · `Burp Suite` · `ffuf` · [OWASP API Top 10](https://owasp.org/www-project-api-security/)
· labs: `crAPI`, `VAmPI`

## 🧪 Ejercicios básicos (individuales)
> Practica en labs deliberadamente vulnerables (crAPI/VAmPI).
1. Con Postman/Burp, explora los endpoints de una API de prueba.
2. Intenta un **IDOR/BOLA**: cambia un `id` y observa si accedes a datos ajenos.
3. Comprueba si la API aplica *rate limiting*.

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Explicar BOLA, BFLA y *excessive data exposure* con ejemplos.
2. Documentar cómo probaron una API de laboratorio.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade endpoints probados, hallazgos y mitigaciones. Firma con tu usuario._
- Endpoint / prueba:
- Hallazgo:
- Aprendizaje clave:
