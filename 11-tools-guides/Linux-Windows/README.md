# Linux y Windows (fundamentos y escalada)

Un pentester debe moverse con soltura en **ambos** sistemas: entender permisos,
servicios, tareas programadas y, sobre todo, las vías comunes de **escalada de
privilegios**. En Linux abundan los binarios SUID y misconfiguraciones; en Windows,
los privilegios de token, servicios inseguros y credenciales guardadas.

## 🛠️ Herramientas habituales
Linux: `linpeas`, [GTFOBins](https://gtfobins.github.io/), `find -perm -4000` ·
Windows: `winpeas`, `PowerUp`, [LOLBAS](https://lolbas-project.github.io/)

## 🧪 Ejercicios básicos (individuales)
> Solo en VMs de laboratorio.
1. Linux: lista binarios SUID (`find / -perm -4000 -type f 2>/dev/null`) y busca
   uno en GTFOBins.
2. Windows: investiga qué revela `whoami /priv` y qué privilegios son peligrosos.
3. Explica el concepto *living off the land* (LOLBins/GTFOBins).

## 👥 Tarea colaborativa en equipo
El grupo debe, en una rama:
1. Crear dos chuletas de enumeración: una Linux y una Windows.
2. Documentar 3 vías de escalada por sistema.
3. Enviar PR (ver [`CONTRIBUTING.md`](../../CONTRIBUTING.md)).

## ✍️ Aportes del equipo (rellenar)
> _Añade comandos de enumeración y vías de escalada. Firma con tu usuario._
| SO | Comando / técnica | Qué consigue |
|---|---|---|
|  |  |  |
