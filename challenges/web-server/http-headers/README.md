# Web - Server — HTTP - Headers

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — HTTP - Headers](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Headers)

La página indica que el contenido no es la única parte relevante de una respuesta HTTP. Al revisar las cabeceras, la instancia revela una cabecera propia relacionada con privilegios de administrador, que luego acepta también desde la petición del cliente.

## Solución

1. Inspeccionar las cabeceras de la respuesta normal:

   ```bash
   curl -i http://challenge01.root-me.org/web-serveur/ch5/
   ```

2. Identificar la cabecera específica de Root-Me y repetir la petición estableciéndola con un valor de acceso:

   ```bash
   curl -H 'Header-RootMe-Admin: true' \\
     http://challenge01.root-me.org/web-serveur/ch5/
   ```

3. La respuesta confirma el acceso y entrega el dato necesario para la validación.
4. Introducir ese dato solamente en Root-Me.

La cuenta ya tenía el reto validado. Se comprobó de nuevo tanto la cabecera indicadora como la respuesta de acceso antes de registrar este writeup.

## Notas adicionales

- Las cabeceras HTTP son datos controlables por el cliente salvo que una infraestructura confiable las agregue y proteja explícitamente.
- Una cabecera enviada por el usuario no puede ser la única prueba de identidad, rol o autorización.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Headers)
- [MDN — HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers)
