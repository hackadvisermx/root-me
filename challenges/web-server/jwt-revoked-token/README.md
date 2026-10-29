# Web - Server — JWT - Revoked token

## Descripción

- **Puntos:** 25
- **Reto:** [Root-Me — JWT - Revoked token](https://www.root-me.org/en/Challenges/Web-Server/JWT-Revoked-token)

La revocación se implementa como comparación literal del JWT completo. Al aceptar representaciones Base64URL equivalentes, el servidor permite reutilizar un token revocado con una codificación distinta que conserva su firma efectiva.

## Solución

1. Iniciar sesión en la instancia y conservar el JWT devuelto.
2. Cerrar sesión para que la aplicación agregue ese token al listado de revocados.
3. Añadir padding Base64URL al final del token, sin modificar ninguno de sus tres segmentos:

   ```bash
   altered_token="${token}="
   ```

4. Solicitar el recurso administrativo con el token equivalente:

   ```bash
   curl -H "Authorization: Bearer ${altered_token}" \
     'http://challenge01.root-me.org/web-serveur/ch63/admin'
   ```

5. Usar el resultado exclusivamente en el formulario de Root-Me.

## Estado de revalidación

La técnica fue contrastada con la lógica publicada del reto y un writeup independiente. Falta reproducirla contra la instancia Start vigente, enviar la respuesta y registrar el «Like»; hasta entonces no se cuenta como validado.

## Notas adicionales

- Una lista de revocación debe identificar el token por un `jti` canónico, no por la cadena serializada completa.
- El servidor debe rechazar codificaciones no canónicas antes de verificar la firma.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Revoked-token)
- [RFC 7519 — JSON Web Token](https://www.rfc-editor.org/rfc/rfc7519)
