# Web - Server — PHP - Filters

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Medium
- **Puntos:** 25
- **Reto:** [Root-Me — PHP - Filters](https://www.root-me.org/en/Challenges/Web-Server/PHP-Filters)

La aplicación incluye un archivo indicado por el parámetro `inc`. Los wrappers de flujo de PHP permiten solicitar un archivo local codificado en Base64 y leer su código fuente sin que el intérprete lo ejecute.

## Solución

1. Confirmar que `inc` controla el archivo incluido por la aplicación.
2. Solicitar el archivo de configuración a través del wrapper `php://filter`:

   ```text
   ?inc=php://filter/read=convert.base64-encode/resource=config.php
   ```

3. Decodificar localmente el contenido recuperado:

   ```bash
   base64 -d config.b64
   ```

4. Usar los valores de configuración solo en el formulario legítimo de la instancia (`?inc=login.php`) y registrar la respuesta únicamente en Root-Me.

La cuenta ya tenía este reto validado. El filtro Base64, la recuperación de configuración y la autenticación de la instancia fueron reproducidos sin versionar datos sensibles.

## Notas adicionales

- Los wrappers de PHP amplían las fuentes que puede abrir una función de inclusión; no deben coexistir con rutas controladas por el usuario.
- Usar identificadores permitidos para las vistas y mantener secretos fuera de archivos accesibles al proceso web cuando sea posible.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Filters)
- [PHP — Supported Protocols and Wrappers](https://www.php.net/manual/en/wrappers.php)
