# Web - Server — SQL injection - Authentication - GBK

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — SQL injection - Authentication - GBK](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-authentication-GBK)

La aplicación escapa comillas con un mecanismo tipo `addslashes()` mientras la conexión usa GBK. Un byte inicial GBK hace que el *backslash* añadido se absorba como parte de un carácter multibyte y deja activa la comilla de la inyección.

## Solución

1. Enviar el formulario como `application/x-www-form-urlencoded`.
2. En el usuario, usar el prefijo multibyte y el comentario MySQL, conservando el espacio final requerido:

   ```text
   1%df%27OR+1%3D1--%20
   ```

3. El cuerpo queda, por ejemplo:

   ```text
   username=1%df%27OR+1%3D1--%20&password=x
   ```

4. Después de escapar la comilla, `0xdf5c` se interpreta como un carácter GBK válido; la comilla posterior sigue siendo sintáctica y la condición `OR 1=1` omite la contraseña.
5. Usar el resultado exclusivamente para validar en Root-Me.

## Estado de revalidación

El vector GBK y la ruta fueron contrastados con análisis públicos. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las consultas parametrizadas son la defensa; escapar manualmente es insuficiente y depende de la codificación.
- La codificación de cliente, conexión y base de datos debe ser consistente.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-authentication-GBK)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
