# Web - Server — PHP - Command injection

## Descripción

> **Enunciado oficial:** “Find a vulnerabilty in this service and exploit it. You must manage to read index.php”.

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 10
- **Autor:** sambecks
- **Reto:** [Root-Me — PHP - Command injection](https://www.root-me.org/en/Challenges/Web-Server/PHP-Command-injection)

La instancia ofrece un formulario para ejecutar `ping` sobre una dirección IP. El valor enviado se concatena a un comando del sistema sin separar los datos del usuario del intérprete de comandos.

## Solución

1. Enviar una IP local válida para confirmar que el formulario ejecuta `ping`.
2. Añadir un separador de comandos y listar el directorio de trabajo:

   ```text
   127.0.0.1; ls
   ```

3. Leer el código pedido por el reto:

   ```text
   127.0.0.1; cat index.php
   ```

4. Como la salida se inserta en la página HTML, inspeccionar el documento si el código no se muestra como texto visible. El código indica que la respuesta se carga desde `.passwd`.
5. Repetir la inyección para leer ese archivo:

   ```text
   127.0.0.1; cat .passwd
   ```

6. Introducir la respuesta obtenida únicamente en el formulario de validación de Root-Me.

La cuenta ya tenía este reto validado. Root-Me confirmó que los 10 puntos ya habían sido obtenidos al repetir el proceso.

## Notas adicionales

- La inyección existe porque un valor controlado por el usuario llega a una shell sin validación estricta ni escapado contextual.
- La mitigación es evitar invocar una shell para esta tarea; si fuera inevitable, se deben usar APIs con argumentos separados y una validación positiva de direcciones IP.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Command-injection)
- [OWASP — OS Command Injection Defense Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/OS_Command_Injection_Defense_Cheat_Sheet.html)
