# Web - Server — HTTP - User-agent

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 10
- **Autor:** g0uZ
- **Reto:** [Root-Me — HTTP - User-agent](https://www.root-me.org/en/Challenges/Web-Server/HTTP-User-agent)

La instancia rechaza la petición normal con el mensaje de que no procede de un navegador `admin`. El reto demuestra que la cabecera HTTP `User-Agent` es un dato enviado por el cliente y puede modificarse libremente.

## Solución

1. Abrir la instancia y observar que una petición con el agente habitual no recibe la respuesta de validación.
2. Repetir la petición declarando `admin` como valor de `User-Agent`.

   ```bash
   curl -A 'admin' http://challenge01.root-me.org/web-serveur/ch2/
   ```

3. La instancia devuelve la respuesta necesaria para validar el reto.
4. Introducirla únicamente en el formulario de validación de Root-Me.

La cuenta ya tenía este reto validado. Root-Me confirmó que los 10 puntos ya habían sido obtenidos al repetir la técnica.

## Notas adicionales

- `User-Agent` sirve para identificar software cliente, no para autorizar usuarios ni proteger recursos.
- La comprobación se puede alterar con DevTools, un proxy HTTP o un cliente como `curl`.
- La protección debe basarse en autenticación y autorización del lado servidor.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-User-agent)
- [MDN — User-Agent request header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/User-Agent)
