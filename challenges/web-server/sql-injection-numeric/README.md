# Web - Server — SQL injection - Numeric

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — SQL injection - Numeric](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Numeric)

Un parámetro numérico no visible en la interfaz se inserta directamente en una consulta SQLite. Al no existir comillas alrededor del valor, se puede ampliar la expresión con un `UNION`.

## Solución

1. Capturar las peticiones de navegación y localizar el parámetro `id`.
2. Probar el número de columnas con una unión controlada, por ejemplo:

   ```sql
   3 UNION SELECT 1,2,3--
   ```

3. Usar `sqlite_master` para localizar la tabla de usuarios y sus columnas.
4. Proyectar los campos requeridos en las posiciones visibles y usar el valor devuelto únicamente en Root-Me.

## Verificación

La enumeración fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- Que un parámetro parezca numérico no lo vuelve seguro: debe estar parametrizado y validado como entero antes de la consulta.
- La cuenta de base de datos debe operar con privilegios mínimos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Numeric)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
