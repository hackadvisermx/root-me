# Web - Server — SQL injection - String

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — SQL injection - String](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-String)

El campo Search se concatena dentro de una búsqueda SQLite `LIKE`. La inyección permite un `UNION` con dos columnas para enumerar el esquema y recuperar la fila necesaria para el reto.

## Solución

1. Confirmar el contexto de cadena con una comilla de diagnóstico.
2. Determinar las dos columnas aceptadas usando un `UNION` inocuo:

   ```sql
   ' UNION SELECT 'safe-probe', NULL -- <espacio>
   ```

3. Consultar `sqlite_master` y `pragma_table_info(...)` para identificar las tablas y columnas relevantes.
4. Usar la consulta resultante sobre la tabla de usuarios únicamente para obtener el valor que Root-Me pide validar.

## Verificación

La enumeración fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- Nunca concatenar búsquedas SQL; parametrizar los valores también en consultas `LIKE`.
- Aplicar autorización de mínimos privilegios a la cuenta de la base de datos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-String)
- [SQLite — SQL Language Expressions](https://sqlite.org/lang_expr.html)
