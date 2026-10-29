# Web - Server — API - Broken Access

## Descripción

> **Enunciado oficial:** “Follow the Swagger!”

- **Categoría:** Web - Server
- **Puntos:** 15
- **Reto:** [Root-Me — API - Broken Access](https://www.root-me.org/en/Challenges/Web-Server/API-Broken-Access)

La plataforma expone documentación Swagger y una API de usuarios y notas. Después de autenticarse con una cuenta propia, la API permite consultar el objeto de otro usuario mediante un identificador predecible.

## Solución

1. Abrir la especificación Swagger en la instancia y enumerar los endpoints `/api/signup`, `/api/login`, `/api/user` y `/api/note`.
2. Crear una cuenta efímera dentro de la instancia de CTF e iniciar sesión.
3. Consultar el identificador administrativo en vez del identificador propio:

   ```bash
   curl -b cookies.txt \
     http://api-broken-access.challenge01.root-me.org/api/user/1
   ```

4. La API devuelve la nota privada sin verificar que el objeto solicitado pertenezca al usuario autenticado.
5. Introducir el valor de la nota solamente en Root-Me.

La respuesta fue aceptada por Root-Me y el reto cambió a palomita. El «Like» quedó registrado.

## Notas adicionales

- Es un caso de IDOR/BOLA: la autenticación no sustituye una comprobación de autorización por objeto.
- Cada endpoint debe verificar que el actor autenticado tiene permiso explícito sobre el recurso solicitado.
- La cuenta de prueba se creó únicamente en la instancia aislada de Root-Me; no se versionan credenciales ni la respuesta.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/API-Broken-Access)
- [OWASP API1:2023 — Broken Object Level Authorization](https://owasp.org/API-Security/editions/2023/en/0xa1-broken-object-level-authorization/)
