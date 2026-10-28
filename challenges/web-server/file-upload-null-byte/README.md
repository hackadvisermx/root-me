# Web - Server — File upload - Null byte

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Medium
- **Puntos:** 25
- **Reto:** [Root-Me — File upload - Null byte](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Null-byte)

La galería valida la extensión de imagen en el nombre de carga, pero no maneja correctamente un byte nulo codificado. La discrepancia permite que el validador vea una extensión permitida mientras el nombre almacenado termina en extensión de script.

## Solución

1. Preparar un archivo de prueba mínimo para el entorno aislado.
2. Enviar un nombre que contenga la extensión de script seguida de `%00` y una extensión de imagen, por ejemplo:

   ```text
   prueba.php%00.jpg
   ```

3. La validación acepta el sufijo de imagen, pero el manejo vulnerable de nombres trunca el archivo en el byte nulo.
4. Abrir el archivo resultante desde la galería y usar la respuesta únicamente para validar en Root-Me.

La cuenta ya tenía este reto validado. La carga con byte nulo codificado fue aceptada y el archivo resultante se interpretó en la instancia oficial.

## Notas adicionales

- Los bytes nulos deben rechazarse o tratarse de forma consistente en todas las capas que reciben, validan y almacenan nombres.
- Las cargas no deben ser ejecutables, aunque un control de extensión falle.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Null-byte)
- [OWASP File Upload Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html)
