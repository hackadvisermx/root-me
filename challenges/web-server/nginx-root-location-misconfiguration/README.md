# Web - Server — Nginx - Root Location Misconfiguration

## Descripción

> **Enunciado oficial:** “Missing Root Location”.

- **Categoría:** Web - Server
- **Puntos:** 15
- **Reto:** [Root-Me — Nginx - Root Location Misconfiguration](https://www.root-me.org/en/Challenges/Web-Server/Nginx-Root-Location-Misconfiguration)

El servidor configura `root /etc/nginx` globalmente y no limita la ruta raíz a contenido público. La regla `location /` permite solicitar archivos de configuración directamente.

## Solución

1. Partir del código Nginx incluido en el enunciado y observar el `root` global.
2. Solicitar la configuración principal:

   ```bash
   curl http://challenge01.root-me.org:59093/nginx.conf
   ```

3. Seguir el `include` indicado por esa configuración:

   ```bash
   curl http://challenge01.root-me.org:59093/conf.d/default.conf
   ```

4. El segundo archivo expone el dato necesario para la validación. Enviarlo únicamente a Root-Me.

La respuesta fue validada en Root-Me y el «Like» quedó registrado.

## Notas adicionales

- La raíz de documentos no debe apuntar a directorios de configuración.
- Una ubicación raíz explícita debe denegar o servir solamente los recursos públicos necesarios.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Nginx-Root-Location-Misconfiguration)
- [NGINX — root directive](https://nginx.org/en/docs/http/ngx_http_core_module.html#root)
