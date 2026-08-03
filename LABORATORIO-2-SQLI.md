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

