# Web - Client — Javascript - Webpack

## Descripción

- **Reto:** [Root-Me — Javascript - Webpack](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Webpack)

La aplicación entrega su lógica como paquetes de Webpack. Aunque el HTML inicial no contiene la respuesta, el bundle de la aplicación conserva información accesible desde el cliente.

## Solución

1. Descargar el HTML de la instancia y localizar el nombre con *hash* del bundle `app`.
2. Recuperar ese JavaScript estático, sin ejecutar código fuera de la instancia autorizada.
3. Revisar el bundle y sus referencias de *source map* para identificar el dato expuesto por la lógica cliente.
4. Usar el resultado únicamente en el formulario de validación de Root-Me.

## Verificación

La solución fue reproducida contra la instancia vigente. La palomita de Root-Me y el «Like» quedaron confirmados; el valor de validación no se versiona.

## Notas adicionales

- Los *bundles* no son un límite de seguridad: su contenido debe tratarse como público.
- Los secretos y decisiones de autorización deben residir del lado del servidor.

