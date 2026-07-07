# Enumeración DNS (DNS Enumeration)

El DNS es la "agenda telefónica" de Internet y **filtra muchísima información**:
servidores de correo, subdominios, infraestructura y a veces configuraciones
erróneas. Enumerar DNS revela buena parte de la superficie de ataque de una
organización.

Un clásico peligroso es la **transferencia de zona (AXFR)** mal configurada, que
puede volcar todos los registros de un dominio de golpe.

## 🛠️ Herramientas habituales
`dig` · `nslookup` · `host` · `dnsenum` · `dnsrecon` · `fierce` · `amass`

## 🧪 Ejercicios básicos (individuales)
1. Con `dig`, consulta los registros `A`, `MX`, `NS` y `TXT` de un dominio de práctica.
2. Explica para qué sirve cada tipo de registro.
3. Prueba una transferencia de zona en un lab: `dig AXFR @<ns> dominio` y explica
   por qué debería estar deshabilitada.

## 👥 Tarea colaborativa en equipo
El grupo de DNS debe, en una rama propia:
1. Documentar cómo enumeraron subdominios (fuerza bruta vs. pasivo).
2. Añadir un mini-glosario de tipos de registro DNS en la sección de abajo.
3. Enviar un PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Completa con comandos, tipos de registro y hallazgos. Firma con tu usuario._
- Comando probado:
- Resultado / interpretación:
- Aprendizaje clave:
