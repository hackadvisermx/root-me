# Web - Server — PHP - type juggling

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — PHP - type juggling](https://www.root-me.org/en/Challenges/Web-Server/PHP-type-juggling)

El endpoint interpreta un objeto JSON controlado por el cliente con comparaciones no estrictas. Al mezclar un booleano y un arreglo, el flujo de autenticación evalúa como verdadero sin comparar una contraseña válida.

## Solución

1. Enviar una petición `POST` URL-encoded a `auth.php`.
2. Colocar el objeto JSON dentro del parámetro `auth`, no en los campos de formulario convencionales:

   ```json
   {"data":{"login":true,"password":[]}}
   ```

3. El booleano satisface la comparación débil del usuario y el arreglo hace que la comprobación no estricta de contraseña falle de forma tratada como éxito por la lógica vulnerable.
4. Usar el resultado del acceso únicamente para la validación del reto.

## Estado de revalidación

La POC fue contrastada contra el endpoint documentado y la evidencia pública de «Access granted». Falta repetirla contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las comprobaciones de identidad deben usar comparaciones estrictas y validación explícita de tipos.
- Los objetos JSON deben validarse con un esquema antes de emplearlos en decisiones de autorización.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-type-juggling)
- [PHP — Comparisons](https://www.php.net/manual/en/types.comparisons.php)
