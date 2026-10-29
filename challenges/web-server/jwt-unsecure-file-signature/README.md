# Web - Server — JWT - Unsecure File Signature

## Descripción

- **Puntos:** 25
- **Reto:** [Root-Me — JWT - Unsecure File Signature](https://www.root-me.org/en/Challenges/Web-Server/JWT-Unsecure-File-Signature)

El encabezado JWT `kid` se usa para elegir el archivo que actúa como clave HMAC. Un filtro incompleto de traversal permite apuntar `kid` a un recurso público de bytes conocidos y firmar un token administrativo válido.

## Solución

1. Obtener el JWT de invitado y conservar la cookie que use la instancia.
2. Descargar el recurso público indicado por la instancia y conservar sus bytes exactos:

   ```bash
   curl -fsS 'http://challenge01.root-me.org:59081/static/challs/htmllecture.html' \
     -o public-key-material
   ```

3. Construir un encabezado `HS256` con un `kid` que evada el filtro literal de `../`:

   ```json
   {"alg":"HS256","kid":"....//static/challs/htmllecture.html","typ":"JWT"}
   ```

4. Cambiar el usuario del *payload* a `admin`, firmar `header.payload` con HMAC-SHA256 usando los bytes descargados y enviar el JWT resultante a `/admin`.
5. Usar el resultado únicamente para validar en Root-Me.

## Estado de revalidación

La técnica fue corroborada contra la documentación del reto. La instancia histórica no estaba disponible durante esta revisión; falta verificarla en la URL Start vigente, enviar la respuesta y registrar el «Like» antes de contarla como validada.

## Notas adicionales

- `kid` debe ser un identificador opaco validado contra una lista permitida; nunca debe resolverse como ruta de archivo controlada por el cliente.
- Una clave criptográfica no debe residir en recursos públicos servidos por la aplicación.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Unsecure-File-Signature)
- [RFC 8725 — JSON Web Token Best Current Practices](https://www.rfc-editor.org/rfc/rfc8725)
