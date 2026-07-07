# 5 · Seguridad de aplicaciones web (Web Application Security)

Las aplicaciones web son hoy la principal superficie de ataque. Este módulo cubre
las vulnerabilidades web más comunes (guiadas por el **OWASP Top 10**) y la
seguridad de **APIs**.

## 🎯 Objetivos de aprendizaje
- Conocer el **OWASP Top 10** y saber reconocer cada categoría.
- Entender inyecciones (SQLi), XSS, control de acceso roto y otras clases.
- Comprender riesgos específicos de **APIs** (OWASP API Top 10).
- Probar de forma metódica siguiendo la guía WSTG.

## 🧠 Conceptos clave
- **Inyección (SQLi/command):** datos no confiables interpretados como código.
- **XSS (Cross-Site Scripting):** ejecución de scripts en el navegador de la víctima.
- **Broken Access Control:** acceder a recursos/acciones sin autorización (IDOR).
- **Autenticación y sesiones:** gestión insegura de credenciales y tokens.
- **API security:** exposición excesiva de datos, falta de rate limiting, BOLA.

## 📁 Material hospedado
- [`OWASP_Top_10.pdf`](OWASP/OWASP_Top_10.pdf) — documento oficial OWASP (licencia abierta).

## 🛠️ Herramientas típicas
`Burp Suite` · `OWASP ZAP` · `sqlmap` · navegador + DevTools · `ffuf`

## 🔗 Recursos
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP API Security Top 10](https://owasp.org/www-project-api-security/)
- [PortSwigger Web Security Academy (gratis)](https://portswigger.net/web-security)
- [OWASP Juice Shop (app para practicar)](https://owasp.org/www-project-juice-shop/)

👉 Practica con los [ejercicios de este módulo](exercises.md).
