# Web - Server — Install files

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — Install files](https://www.root-me.org/en/Challenges/Web-Server/Install-files)

El código fuente de la página inicial deja una referencia a una instalación de phpBB. La aplicación conserva su instalador en una ruta que sigue accesible desde el servidor web.

## Solución

1. Revisar el código fuente de la página de inicio para identificar el directorio de la aplicación instalada.
2. Recorrer únicamente la ruta indicada hasta el instalador:

   ```bash
   curl http://challenge01.root-me.org/web-serveur/ch6/phpbb/install/install.php
   ```

3. El instalador expuesto muestra el dato requerido para completar el reto.
4. Introducirlo exclusivamente en Root-Me.

La cuenta ya tenía este reto validado. La ruta de instalación y la respuesta de la instancia se comprobaron de nuevo antes de documentarlo.

## Notas adicionales

- Los instaladores pueden permitir reconfigurar una aplicación, restablecer credenciales o exponer información sensible.
- Deben eliminarse o bloquearse tras el despliegue, y no quedar accesibles desde el directorio público.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Install-files)
- [OWASP WSTG — Testing for Backup and Unreferenced Files](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/08-Testing_for_Backup_and_Unreferenced_Files)
