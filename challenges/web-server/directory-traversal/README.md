# Web - Server — Directory traversal

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Medium
- **Puntos:** 25
- **Reto:** [Root-Me — Directory traversal](https://www.root-me.org/en/Challenges/Web-Server/Directory-traversal)

La aplicación selecciona una galería mediante un parámetro de ruta. Al consultar una galería no prevista, publica una referencia a un archivo sensible sin restringir de forma adecuada la ruta accesible.

## Solución

1. Observar que el parámetro `galerie` controla el contenido cargado por la aplicación.
2. Enumerar rutas permitidas de forma acotada dentro de la instancia hasta localizar un directorio no previsto.
3. Consultar la galería encontrada:

   ```text
   /web-serveur/ch15/ch15.php?galerie=<directorio-encontrado>
   ```

4. Seguir la referencia a `password.txt` que devuelve la aplicación y usar el dato solo para validar el reto.

La cuenta ya tenía este reto validado. Se comprobó de nuevo el acceso al directorio y la recuperación del archivo referido.

## Notas adicionales

- El servidor debe permitir únicamente identificadores de recursos esperados, no rutas suministradas por el cliente.
- Las rutas se deben normalizar y validar antes de acceder al sistema de archivos.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Directory-traversal)
- [OWASP — Path Traversal](https://owasp.org/www-community/attacks/Path_Traversal)
