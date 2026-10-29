# Web - Server — SQL injection - Time based

## Descripción

- **Puntos:** 45
- **Reto:** [Root-Me — SQL injection - Time based](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Time-based)

El punto de inyección no muestra resultados ni errores útiles. La aplicación permite inferir condiciones observando una demora deliberada de la base de datos.

## Solución

1. Capturar una petición estable de la instancia Start y medir varias veces su tiempo base de respuesta.
2. Probar una condición verdadera y otra falsa que solo difieran en la demora inducida, ajustada al motor identificado.
3. Extraer el dato objetivo con preguntas binarias de longitud y caracteres, usando un umbral de tiempos y repeticiones para reducir ruido.
4. Validar únicamente el valor solicitado por el reto en Root-Me y registrar el «Like».

## Estado de revalidación

El canal temporal y el parámetro vulnerable fueron corroborados con writeups públicos. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las consultas parametrizadas previenen la inyección; los mensajes de error suprimidos no sustituyen esa medida.
- Limitar tiempos de ejecución y monitorizar anomalías reduce el impacto de este tipo de canal lateral.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Time-based)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
