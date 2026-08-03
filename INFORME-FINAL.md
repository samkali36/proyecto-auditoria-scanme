# Proyecto 1: Auditoría Externa - Sam Esparza
Fecha: 3 Ago 2026 | Objetivo: scanme.nmap.org 45.33.32.156
Herramientas: Kali WSL + Nikto 2.6.0
Hallazgos:
1. Apache 2.4.7 desactualizado (Actual es 2.4.66)
2. Faltan cabeceras: strict-transport-security, content-security-policy, etc
3. mod_negotiation habilitado

Evidencia: mi-primer-escaneo.txt y nikto.txt (629 requests, 20 errores, 9 hallazgos)
