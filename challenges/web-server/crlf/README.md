# Web - Server — CRLF

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Easy
- **Puntos:** 20
- **Reto:** [Root-Me — CRLF](https://www.root-me.org/en/Challenges/Web-Server/CRLF)

La instancia registra los intentos de autenticación y usa el nombre de usuario en esa salida. Al no neutralizar retornos de carro y saltos de línea, un valor controlado permite inyectar una nueva entrada en el registro.

## Solución

1. Enviar un intento normal y observar el formato de las líneas del registro.
2. Construir un valor `username` que contenga una línea de éxito seguida por `%0d%0a` y otro nombre de usuario:

   ```text
   admin authenticated.%0d%0aguest
   ```

3. Enviarlo codificado en la petición de la instancia:

   ```bash
   curl 'http://challenge01.root-me.org/web-serveur/ch14/?username=admin%20authenticated.%0d%0aguest&password=123'
   ```

4. La nueva línea inyectada satisface la condición del reto y expone el dato de validación.
5. Usar ese dato únicamente en Root-Me.

La cuenta ya tenía este reto validado. La inyección y la respuesta de la instancia se reprodujeron antes de documentarlo.

## Notas adicionales

- CRLF representa `\r\n`, el separador de líneas usado por varios protocolos y formatos de texto.
- Los registros deben codificar o eliminar caracteres de control de toda entrada no confiable y conservar un formato estructurado.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/CRLF)
- [OWASP — CRLF Injection](https://owasp.org/www-community/vulnerabilities/CRLF_Injection)
