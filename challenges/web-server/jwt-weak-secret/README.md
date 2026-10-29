# Web - Server — JWT - Weak secret

## Descripción

- **Puntos:** 25
- **Reto:** [Root-Me — JWT - Weak secret](https://www.root-me.org/en/Challenges/Web-Server/JWT-Weak-secret)

El JWT de invitado usa HMAC con una clave débil. Una vez comprobada su contraseña de firma mediante un diccionario autorizado, el atacante puede emitir un token válido con el rol administrativo.

## Solución

1. Obtener el JWT de invitado desde el endpoint `token`.
2. Confirmar el algoritmo HMAC indicado en su encabezado; la instancia usa `HS512`.
3. Someter únicamente el JWT de la instancia de CTF a un ataque de diccionario autorizado y recuperar la clave débil.
4. Firmar de nuevo un token `HS512`, cambiando solo el *claim* de rol a `admin`.
5. Enviar el token resultante como Bearer al endpoint administrativo:

   ```bash
   curl -X POST -H "Authorization: Bearer ${jwt_admin}" \
     'http://challenge01.root-me.org/web-serveur/ch59/admin'
   ```

6. Usar el resultado exclusivamente para la validación en Root-Me.

## Estado de revalidación

La estructura de los endpoints y el vector de clave débil fueron reproducidos en segundo plano. Falta enviar la respuesta autenticada y registrar el «Like» en Root-Me; hasta entonces no se cuenta como validado.

## Notas adicionales

- Las claves HMAC deben tener entropía suficiente y gestionarse fuera del código y de diccionarios previsibles.
- La clave y la respuesta no se versionan.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Weak-secret)
- [RFC 8725 — JSON Web Token Best Current Practices](https://www.rfc-editor.org/rfc/rfc8725)
