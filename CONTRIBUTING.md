# 🤝 Guía de colaboración (para alumnos)

¡Bienvenido/a! Este repositorio es **colaborativo**. Parte del curso es aprender a
trabajar en equipo con **Git y GitHub**, igual que en un trabajo real. Cada
subcarpeta (Nmap, OSINT, Burp-Suite, ...) es una **estación**: un equipo la
"adopta", investiga y **rellena la sección _Aportes del equipo_** con lo que
aprende.

> 🎯 **Regla de oro:** todo lo que publiques aquí debe ser **contenido propio** o
> enlaces a fuentes oficiales. Nunca subas PDFs o textos con copyright de terceros.

## ✅ Requisitos previos (hazlo una sola vez)

1. **Crea tu cuenta gratuita** en [github.com](https://github.com/) y elige un
   usuario (lo usarás para firmar tus aportes).
2. **Envía tu usuario de GitHub al instructor** para que te agregue como
   colaborador del repositorio.
3. **Acepta la invitación:** te llegará por correo y también en
   `github.com/notifications`. Hasta que la aceptes, no podrás subir ramas.
4. Instala [Git](https://git-scm.com/downloads) en tu equipo.

> 👤 **Para el instructor:** agrega a cada alumno en
> **Settings → Collaborators and teams → Add people** con su usuario de GitHub.
> En repos públicos es gratis e ilimitado.

## 🧭 Flujo de trabajo (paso a paso)

### 1. Clona el repositorio
```bash
git clone https://github.com/alejandroromero-bit/security-pt-course1.git
cd security-pt-course1
```

### 2. Crea tu rama de trabajo
Nunca trabajes directamente sobre `main`. Crea una rama con tu equipo/tema:
```bash
git checkout -b nmap-equipo-azul
```

### 3. Edita tu estación
Abre el `README.md` de tu subcarpeta y completa la sección **✍️ Aportes del
equipo** con comandos, hallazgos y aprendizajes. Firma con tu usuario de GitHub.

### 4. Guarda tus cambios (commit)
```bash
git add .
git commit -m "Nmap: añado tabla de flags y 2 comandos NSE (@tu-usuario)"
```

### 5. Sube tu rama
```bash
git push origin nmap-equipo-azul
```

### 6. Abre un Pull Request (PR)
En GitHub, pulsa **"Compare & pull request"**, describe qué añadiste y solicita
revisión. El instructor u otro equipo lo revisa y lo fusiona a `main`.

## ✅ Buenas prácticas
- **Commits pequeños y con mensaje claro** (qué y por qué).
- Un PR = un tema. No mezcles varias estaciones en el mismo PR.
- Revisa el trabajo de otros equipos y comenta con respeto.
- Si algo se rompe, no pasa nada: para eso están las ramas. 🙂

## 🧩 Ejercicio en equipo sugerido
1. Cada equipo elige (o se le asigna) **una estación**.
2. Investiga y completa su sección de aportes.
3. Abre un PR y **revisa el PR de otro equipo**.
4. Puesta en común: cada equipo presenta su estación al resto.

Así aprendéis el tema **y** el flujo profesional de GitHub a la vez. 🚀
