# Cryptanalysis — Hash - Message Digest 5

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — Hash - Message Digest 5](https://www.root-me.org/en/Challenges/Cryptanalysis/Hash-Message-Digest-5)

El reto proporciona una huella MD5 de un valor corto. MD5 es una función hash de una vía, por lo que se compara contra candidatos o una lista autorizada.

## Solución

1. Identificar la huella por su formato hexadecimal de 32 caracteres.
2. Probar candidatos de forma local y controlada:

   ```bash
   printf '%s' '<candidato>' | md5sum
   ```

3. Comparar la salida con la huella del reto y enviar únicamente la coincidencia a Root-Me.

La cuenta conserva la validación y se registró «Like». No se almacenan la entrada ni la respuesta.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cryptanalysis/Hash-Message-Digest-5)
- [RFC 1321 — MD5](https://www.rfc-editor.org/rfc/rfc1321)
