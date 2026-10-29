# Web - Server — PHP - Apache configuration

## Descripción

- **Puntos:** 25
- **Reto:** [Root-Me — PHP - Apache configuration](https://www.root-me.org/en/Challenges/Web-Server/PHP-Apache-configuration)

El filtro de subida prohíbe extensiones PHP, pero acepta `.htaccess` en un directorio escribible que permite `AllowOverride`. Esto permite asociar un nombre sin extensión a un manejador PHP.

## Solución

1. Subir un archivo `.htaccess` a la carpeta temporal de la sesión. La configuración habilita el motor PHP y asocia un nombre inocuo al manejador `application/x-httpd-php`:

   ```apache
   Options +Indexes

   <IfModule mod_php7.c>
     php_flag engine on
   </IfModule>

   <FilesMatch "^viewer$">
     SetHandler application/x-httpd-php
   </FilesMatch>
   ```

2. Usar el listado temporal solo para identificar la carpeta de carga.
3. Subir el archivo `viewer`, sin extensión PHP, con una lectura del recurso objetivo relativa a esa carpeta.
4. Abrir `viewer`; Apache lo ejecuta como PHP por la regla de `.htaccess`.
5. Usar el resultado exclusivamente para validar en Root-Me.

## Estado de revalidación

La técnica fue contrastada con el comportamiento y configuración documentados del reto. La instancia histórica no respondió durante esta revisión; falta reproducirla en la URL Start vigente, validar y registrar el «Like».

## Notas adicionales

- Las carpetas de carga no deben permitir `AllowOverride`, listado de directorio ni ejecución de scripts.
- La validación de cargas debe usar una lista permitida real, almacenamiento fuera de la raíz web y nombres generados por el servidor.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Apache-configuration)
- [Apache HTTP Server — .htaccess Files](https://httpd.apache.org/docs/current/howto/htaccess.html)
