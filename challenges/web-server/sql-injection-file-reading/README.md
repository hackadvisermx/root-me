# Web - Server — SQL injection - File reading

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — SQL injection - File reading](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-file-reading)

Una consulta vulnerable permite invocar una capacidad del motor de base de datos que lee archivos accesibles para el proceso. El objetivo es demostrar el impacto de una inyección más allá de las tablas.

## Solución

1. Identificar el parámetro vulnerable y el motor de base de datos mediante respuestas controladas de la instancia Start.
2. Establecer el número de columnas y la posición visible, evitando consultas ajenas al objetivo del reto.
3. Confirmar la capacidad de lectura con un recurso inofensivo expuesto por el propio reto antes de solicitar el archivo objetivo indicado.
4. Enviar el resultado únicamente al formulario de validación de Root-Me.

## Estado de revalidación

El uso de una función de lectura de archivos desde SQL fue corroborado con un writeup público. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las cuentas de base de datos no deben disponer de privilegios de lectura arbitraria del sistema de archivos.
- Las consultas deben ser parametrizadas y el usuario de aplicación debe tener privilegios mínimos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-file-reading)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
