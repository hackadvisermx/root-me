# Web - Client — Javascript - Authentication 2

## Descripción

- **Dificultad:** Easy
- **Puntos:** 10
- **Reto:** [Root-Me — Javascript - Authentication 2](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Authentication-2)

Una segunda autenticación del lado cliente construye el valor aceptado mediante JavaScript; separar o concatenar cadenas no convierte una credencial en secreta.

## Solución

1. Localizar `login.js` desde el HTML de la instancia.
2. Seguir cómo se construye el valor que compara la función de autenticación, en vez de intentar adivinarlo.
3. Introducir el resultado en el formulario y validarlo solamente en Root-Me.

## Estado de revalidación

La cuenta conserva el reto validado y recibió «Like». El endpoint histórico responde sin el formulario y scripts originales, por lo que este writeup es una reconstrucción retroactiva sin exponer la credencial.

## Notas adicionales

- Ofuscar, dividir o generar una contraseña en cliente no reemplaza la autenticación de servidor.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Authentication-2)
- [OWASP — Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
