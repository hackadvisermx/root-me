# Web - Client — Javascript - Authentication

## Descripción

- **Dificultad:** Easy
- **Puntos:** 5
- **Reto:** [Root-Me — Javascript - Authentication](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Authentication)

La comprobación de usuario y contraseña se realiza enteramente en `login.js`; por tanto, ambos valores son accesibles para quien descarga el cliente.

## Solución

1. Abrir las herramientas de desarrollo y localizar `login.js`.
2. Seguir la función que compara los campos `pseudo` y `password` hasta los valores literales que acepta.
3. Introducir esos valores en el formulario de la instancia y usar el resultado solo en Root-Me.

## Estado de revalidación

La cuenta mantiene el reto validado y recibió su «Like». La instancia histórica ya no entrega el script original de forma navegable, así que la técnica se documenta como reconstrucción retroactiva sin guardar credenciales ni respuesta.

## Notas adicionales

- Ningún secreto ni autorización debe residir en JavaScript enviado al navegador.
- La validación debe realizarse en el servidor.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Authentication)
- [OWASP — Client-side Security](https://owasp.org/www-community/controls/Client-side_Security)
