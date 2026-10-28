# Web - Server — Backup file

## Descripción

> **Enunciado oficial:** “No clue.”

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 10
- **Reto:** [Root-Me — Backup file](https://www.root-me.org/en/Challenges/Web-Server/Backup-file)

La instancia presenta un formulario de autenticación sin pistas. El nombre del reto dirige la revisión hacia copias de seguridad expuestas por el servidor web: suelen conservar código fuente o datos de configuración que no deberían ser públicos.

## Solución

1. Confirmar que la página de inicio corresponde a `index.php`.
2. Probar nombres de respaldo habituales del archivo de inicio. En este caso, la copia creada con el sufijo de respaldo de Vim está expuesta:

   ```bash
   curl -O http://challenge01.root-me.org/web-serveur/ch11/index.php~
   ```

3. Revisar el archivo descargado localmente. El código fuente contiene los valores usados por el formulario de autenticación.
4. Enviarlos al formulario de la instancia y comprobar que se muestra el mensaje de validación.
5. Introducir únicamente la respuesta obtenida en el formulario de validación de Root-Me.

La cuenta ya tenía este reto validado. Al repetir la técnica, la instancia aceptó la autenticación y Root-Me confirmó que los 10 puntos ya habían sido obtenidos.

## Notas adicionales

- Los sufijos de respaldo que deja un editor son una fuente habitual de exposición de código; el sufijo `~` es una convención frecuente en copias de Vim.
- El análisis debe empezar por nombres concretos y razonables, sin convertir el ejercicio autorizado en un escaneo indiscriminado.
- En un despliegue real, los respaldos no deben quedar bajo el directorio publicado por el servidor web y deben contener secretos fuera del código fuente.
- Las credenciales y la respuesta de validación no se versionan.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Backup-file)
- [OWASP Testing Guide — Backup and Unreferenced Files](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/08-Testing_for_Backup_and_Unreferenced_Files)
