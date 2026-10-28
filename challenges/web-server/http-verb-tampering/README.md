# Web - Server — HTTP - Verb tampering

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — HTTP - Verb tampering](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Verb-tampering)

El recurso usa autenticación HTTP para una petición habitual, pero su protección no se aplica de igual forma a todos los métodos HTTP. Una petición con un método alternativo alcanza contenido que no debería ser público.

## Solución

1. Confirmar que una petición normal recibe el reto de autenticación.
2. Repetir la solicitud con un método HTTP alternativo autorizado dentro de la instancia:

   ```bash
   curl -X PUT http://challenge01.root-me.org/web-serveur/ch8/
   ```

3. La respuesta permite recuperar el dato requerido por el reto.
4. Usarlo solo para validar en Root-Me.

La cuenta ya tenía este reto validado. La instancia volvió a aceptar el método alternativo antes de registrar el writeup.

## Notas adicionales

- Los controles de autenticación y autorización deben aplicarse de forma coherente a todos los métodos que expone el servidor.
- Si la aplicación no necesita métodos como `PUT`, conviene deshabilitarlos explícitamente.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Verb-tampering)
- [OWASP WSTG — Testing for HTTP Verb Tampering](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/07-Input_Validation_Testing/03-Testing_for_HTTP_Verb_Tampering)
