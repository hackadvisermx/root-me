# Web - Server — SQL injection - Authentication

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — SQL injection - Authentication](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-authentication)

El formulario concatena el nombre de usuario en una consulta SQL de autenticación. El cierre de la cadena y un comentario SQL eliminan la condición de contraseña.

## Solución

1. Abrir el formulario de inicio de sesión de la instancia del reto.
2. En el usuario, cerrar la cadena y comentar la condición posterior:

   ```text
   admin'-- <espacio>
   ```

3. Conservar el espacio final cuando el motor SQL lo requiera y colocar un valor cualquiera en contraseña.
4. La consulta resultante selecciona la cuenta objetivo sin evaluar la contraseña. Usar el resultado solo para validar en Root-Me.

## Estado de revalidación

El vector y el endpoint fueron contrastados con documentación pública del reto. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- La defensa correcta son consultas preparadas con parámetros, no el filtrado manual de comillas o comentarios.
- Las cuentas de pruebas deben limitarse al entorno CTF autorizado.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-authentication)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
