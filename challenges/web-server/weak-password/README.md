# Web - Server — Weak password

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 10
- **Autor:** g0uZ
- **Reto:** [Root-Me — Weak password](https://www.root-me.org/en/Challenges/Web-Server/Weak-password)

La instancia protege el recurso con autenticación HTTP Basic. El objetivo es identificar una credencial débil y usarla para acceder a la respuesta de validación.

## Solución

1. Abrir la instancia y comprobar que responde con una petición de autenticación HTTP Basic.
2. Probar la credencial débil prevista por el reto, únicamente contra la instancia autorizada.
3. Al autenticarse, la página confirma que la contraseña usada sirve para validar el reto.
4. Introducir esa respuesta solo en el formulario oficial de Root-Me.

La cuenta ya tenía este reto validado. Root-Me confirmó que los 10 puntos ya habían sido obtenidos al repetir la autenticación correcta.

## Notas adicionales

- Las credenciales no se incluyen en el repositorio, incluso cuando sean deliberadamente débiles y formen parte del reto.
- HTTP Basic transmite las credenciales codificadas en Base64, no cifradas; debe usarse exclusivamente sobre HTTPS y con contraseñas robustas.
- En sistemas reales se deben aplicar políticas de contraseñas, límites de intentos y autenticación multifactor cuando corresponda.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Weak-password)
- [MDN — HTTP authentication](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Authentication)
