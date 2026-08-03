# 🛡️ Portafolio de Ciberseguridad - Sam Esparza
![Kali](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![OWASP](https://img.shields.io/badge/OWASP-A03_Injection-red?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-DVWA-blue?style=for-the-badge&logo=docker)

Auditorías y laboratorios prácticos enfocados en Pentesting Web y Auditoría Externa.
Entorno: Kali Linux WSL + Docker | Metodología: OWASP Top 10

## 📋 Laboratorios

| # | Proyecto | Hallazgo | Herramientas | Riesgo |
|---|---|---|---|---|
| 1 | Auditoría Externa - scanme.nmap.org | Apache 2.4.7 desactualizado, falta de cabeceras HSTS/CSP | Nmap, Nikto | Alto |
| 2 | SQL Injection - DVWA | Bypass con ' OR '1'='1 y extracción de hashes MD5 vía UNION SELECT | Burp Suite, SQLi, Docker | Crítico |

## 🎯 Lab Destacado: SQL Injection

*Payloads usados:*
- 1' OR '1'='1 -> Bypass y dump de usuarios
- 1' UNION SELECT user,password FROM users# -> Extracción de credenciales

*Credenciales obtenidas:*
- admin:5f4dcc3b5aa765d61d8327deb882cf99 (password)
- gordonb:e99a18c428cb38d5f260853678922e03 (abc123)

*Mitigación:* Implementar Prepared Statements y validación de entradas.

---
*Autor:* Sam Esparza Morga - Monterrey, N.L. | Fecha: Ago 2026
*Objetivo:* Posición Jr. Pentester / Analista SOC
