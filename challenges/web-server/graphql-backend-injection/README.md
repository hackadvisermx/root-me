# Web - Server — GraphQL - Backend injection

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — GraphQL - Backend injection](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Backend-injection)

El argumento `id` de una consulta GraphQL llega sin parametrizar al backend SQL. La sintaxis GraphQL limita el punto de entrada, pero no evita una inyección SQL en el resolvedor.

## Solución

1. Usar introspección para obtener el tipo `rocket`, sus campos visibles y el argumento `id`.
2. Confirmar que `id` llega a un contexto SQL y ajustar el número de columnas a los campos GraphQL solicitados.
3. Enumerar primero metadatos con `information_schema` y luego consultar el valor objetivo a través de un `UNION` que alinee sus columnas con la respuesta `rocket`.
4. Usar el valor devuelto exclusivamente para validar en Root-Me.

## Estado de revalidación

El endpoint `/rocketql`, el campo vulnerable y la técnica de unión fueron verificados mediante un writeup público. Falta reproducir el flujo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- GraphQL no sustituye las consultas parametrizadas: cada resolvedor debe enlazar parámetros en el backend.
- Limitar la introspección y la exposición de errores reduce la superficie de enumeración, pero no corrige la inyección.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Backend-injection)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
