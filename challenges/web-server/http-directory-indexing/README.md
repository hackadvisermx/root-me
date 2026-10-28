# Web - Server — HTTP - Directory indexing

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — HTTP - Directory indexing](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Directory-indexing)

El directorio inicial deja una pista en el código HTML hacia una ruta administrativa. Al visitar sus directorios sin archivo índice, el servidor publica sus nombres y permite recorrer hasta un archivo sensible.

## Solución

1. Revisar el HTML de la página inicial y localizar la referencia a la ruta administrativa.
2. Solicitar el directorio, en vez de solo el archivo indicado por la pista:

   ```bash
   curl http://challenge01.root-me.org/web-serveur/ch4/admin/
   ```

3. La respuesta lista un subdirectorio de respaldos. Consultarlo para identificar el archivo publicado:

   ```bash
   curl http://challenge01.root-me.org/web-serveur/ch4/admin/backup/
   ```

4. Recuperar el contenido del archivo listado y utilizarlo exclusivamente para validar el reto en Root-Me.

La cuenta ya tenía el reto validado. La ruta, los índices de directorio y la respuesta de la instancia fueron reproducidos antes de documentarlo.

## Notas adicionales

- El listado automático de directorios revela estructura interna y archivos que no estaban destinados a ser accesibles.
- Es preferible desactivarlo en el servidor y aplicar controles de acceso a directorios administrativos y respaldos.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Directory-indexing)
- [Apache HTTP Server — mod_autoindex](https://httpd.apache.org/docs/2.4/mod/mod_autoindex.html)
