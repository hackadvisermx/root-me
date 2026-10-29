# Web - Server — JWT - Introduction

## Descripción

- **Puntos:** 20
- **Reto:** [Root-Me — JWT - Introduction](https://www.root-me.org/en/Challenges/Web-Server/JWT-Introduction)

La aplicación acepta un JWT sin firma al confiar en el encabezado `alg` controlado por el cliente. Así se puede alterar la identidad declarada sin que el servidor verifique una firma criptográfica.

## Solución

1. Obtener el JWT de invitado y decodificar sin modificar la evidencia original.
2. Construir un token con encabezado y *payload* administrativos:

   ```json
   {"typ":"JWT","alg":"none"}
   ```

   ```json
   {"username":"admin"}
   ```

3. Conservar el separador final de la firma vacía y enviar el token como cookie `jwt` a `index.php`.
4. Usar el resultado del panel administrativo únicamente para validar en Root-Me.

## Estado de revalidación

La instancia confirmó el acceso administrativo con el token sin firma. Falta enviar la respuesta autenticada y registrar el «Like» en Root-Me; hasta entonces no se cuenta como validado.

## Notas adicionales

- El algoritmo debe fijarse del lado del servidor y validarse antes de procesar el token.
- Deben rechazarse explícitamente `alg: none`, firmas vacías y algoritmos no incluidos en una lista permitida.
- No se versiona la respuesta.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Introduction)
- [RFC 8725 — JSON Web Token Best Current Practices](https://www.rfc-editor.org/rfc/rfc8725)
