# Proyecto 1: Auditoría Externa - scanme.nmap.org
*Autor:* Sam Esparza | *Fecha:* 3 Ago 2026

Objetivo legal de práctica: scanme.nmap.org (45.33.32.156)

### Herramientas
Kali Linux WSL + Nikto 2.6.0

### Hallazgos
1. Apache 2.4.7 desactualizado (actual 2.4.66) - Riesgo alto
2. Faltan cabeceras de seguridad: HSTS, CSP, X-Frame-Options
3. mod_negotiation habilitado - enumeración de archivos

### Evidencia
- nikto.txt: 629 requests, 488 seg, 9 hallazgos
- mi-primer-escaneo.txt

### Mitigación
Actualizar Apache, implementar cabeceras, deshabilitar negociación.
