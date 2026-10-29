# Web - Server — SQL injection - Error

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — SQL injection - Error](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Error)

Un parámetro de ordenamiento se concatena en una consulta SQL. Los mensajes de error que devuelve la aplicación revelan que ese valor llega al motor sin una lista cerrada de opciones.

## Solución

1. Capturar una petición válida de la instancia Start que use el parámetro de orden.
2. Comprobar el punto de inyección con una variación sintáctica mínima y comparar el error con la respuesta normal.
3. Determinar el motor y la forma de la consulta con pruebas de bajo impacto; usar un cliente de repetición o automatización únicamente contra esta instancia CTF.
4. Enumerar exclusivamente la información necesaria para el objetivo del reto y validar el valor recuperado en Root-Me.

## Estado de revalidación

El parámetro `order` y el flujo de error fueron corroborados con un writeup público. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Los identificadores SQL, como orden y columnas, requieren una lista cerrada; los valores deben ir como parámetros preparados.
- Los errores detallados del motor no deben enviarse al cliente.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Error)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
