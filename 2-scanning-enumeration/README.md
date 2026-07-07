# 2 · Escaneo y enumeración (Scanning & Enumeration)

Tras el reconocimiento, el escaneo identifica **qué hosts están vivos**, **qué
puertos están abiertos** y **qué servicios/versiones** corren en ellos. La
enumeración profundiza en cada servicio para extraer detalles útiles.

## 🎯 Objetivos de aprendizaje
- Descubrir hosts activos en una red.
- Escanear puertos TCP/UDP e interpretar estados (`open`, `closed`, `filtered`).
- Detectar servicios y versiones (banner grabbing).
- Usar el motor de scripts de Nmap (NSE) para enumeración.

## 🧠 Conceptos clave
- **Host discovery:** determinar qué IPs responden (`nmap -sn`).
- **Escaneo de puertos:** SYN scan (`-sS`), connect scan (`-sT`), UDP (`-sU`).
- **Detección de versión y SO:** `-sV`, `-O`.
- **NSE (Nmap Scripting Engine):** scripts para enumerar y detectar vulnerabilidades.
- **Ruido vs. sigilo:** un escaneo agresivo (`-T4/-T5`) es rápido pero detectable.

## 🛠️ Herramientas típicas
`nmap` · `masscan` · `netcat` · `rustscan` · scripts NSE

## 🔗 Recursos
- [Nmap — Libro oficial (gratis)](https://nmap.org/book/) · [Guía de referencia](https://nmap.org/book/man.html)
- [HackTricks — Pentesting de red](https://book.hacktricks.xyz/)
- [MITRE ATT&CK — Discovery](https://attack.mitre.org/tactics/TA0007/)

👉 Practica con los [ejercicios de este módulo](exercises.md).
