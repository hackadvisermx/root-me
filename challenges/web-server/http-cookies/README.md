# Web - Server — HTTP - Cookies

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Easy
- **Puntos:** 20
- **Reto:** [Root-Me — HTTP - Cookies](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Cookies)

La aplicación mantiene el rol de visitante en una cookie legible y deja que el cliente decida su valor. Al sustituir el valor de rol por el de administrador, el servidor revela el contenido reservado.

## Solución

1. Inspeccionar las cookies devueltas por la página después de una interacción normal.
2. Identificar la cookie que representa el rol y enviar una nueva petición con el valor de administrador:

   ```bash
   curl -H 'Cookie: ch7=admin' \\
     http://challenge01.root-me.org/web-serveur/ch7/
   ```

3. La respuesta de la instancia confirma el acceso y contiene el dato de validación.
4. Introducirlo únicamente en Root-Me.

La cuenta ya tenía este reto validado. La cookie manipulada volvió a permitir el acceso antes de registrar el writeup.

## Notas adicionales

- Las cookies son valores del lado cliente; no deben contener decisiones de autorización sin protección criptográfica y validación de servidor.
- El control de acceso debe partir de una sesión opaca o de datos verificables del lado servidor.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Cookies)
- [OWASP — Session Management Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html)
