# Web - Server — File upload - MIME type

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Easy
- **Puntos:** 20
- **Reto:** [Root-Me — File upload - MIME type](https://www.root-me.org/en/Challenges/Web-Server/File-upload-MIME-type)

La galería bloquea un archivo de script por su tipo declarado, pero toma el valor `Content-Type` del formulario como una fuente confiable. Ese valor lo controla el cliente y puede presentarse como el de una imagen.

## Solución

1. Abrir el formulario de carga y comprobar que rechaza un archivo de script con su tipo habitual.
2. Enviar un archivo de prueba con extensión de script, pero declarar en la parte multipart un tipo de imagen, por ejemplo `image/gif`:

   ```bash
   curl -X POST \\
     -F 'file=@prueba.php;type=image/gif' \\
     'http://challenge01.root-me.org/web-serveur/ch21/?action=upload'
   ```

3. Abrir el archivo aceptado desde la galería para confirmar que el servidor lo interpreta.
4. Usar el dato recuperado solo en el formulario de validación de Root-Me.

La cuenta ya tenía este reto validado. Se comprobó nuevamente que el tipo MIME controlado por el cliente basta para cargar e interpretar el archivo de prueba.

## Notas adicionales

- `Content-Type` de una petición multipart es un metadato declarado por el cliente, no una garantía sobre el contenido.
- La defensa combina validación del contenido, nombres generados por el servidor, almacenamiento fuera de la raíz pública y ausencia de permisos de ejecución.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/File-upload-MIME-type)
- [OWASP File Upload Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html)
