# Web - Server — File upload - Double extensions

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Easy
- **Puntos:** 20
- **Reto:** [Root-Me — File upload - Double extensions](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Double-extensions)

La galería permite subir archivos que terminan con una extensión de imagen. Esa comprobación no considera que el servidor pueda interpretar una extensión anterior como código ejecutable.

## Solución

1. Abrir la sección de carga de la galería y confirmar que rechaza un archivo de script con una sola extensión.
2. Preparar un archivo de prueba mínimo para el entorno del reto y nombrarlo con doble extensión, por ejemplo `prueba.php.jpg`.
3. Subirlo como imagen a la ruta de carga de la instancia:

   ```text
   /web-serveur/ch20/?action=upload
   ```

4. Abrir el archivo desde la galería. El servidor interpreta la extensión de script anterior y permite recuperar el dato de validación del entorno aislado.
5. Introducirlo solo en Root-Me.

La cuenta ya tenía este reto validado. Se confirmó de nuevo que la carga con doble extensión es aceptada y que el servidor interpreta el archivo resultante.

## Notas adicionales

- La validación basada solo en el nombre original o en una lista de sufijos finales no basta para proteger una carga de archivos.
- Las cargas deben almacenarse fuera del directorio ejecutable, con un nombre generado por el servidor y sin permisos de ejecución.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Double-extensions)
- [OWASP File Upload Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html)
