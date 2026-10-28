# Cryptanalysis — Hash - SHA-2

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — Hash - SHA-2](https://www.root-me.org/en/Challenges/Cryptanalysis/Hash-SHA-2)

El reto usa una familia SHA-2; su longitud permite distinguir SHA-224, SHA-256, SHA-384 o SHA-512 antes de comparar candidatos.

## Solución

1. Identificar el algoritmo por el tamaño de la huella hexadecimal.
2. Calcular la variante correspondiente sobre candidatos locales:

   ```bash
   printf '%s' '<candidato>' | sha256sum
   ```

3. Comparar la huella y enviar el único resultado a Root-Me.

La cuenta ya lo tenía validado y se registró «Like». La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cryptanalysis/Hash-SHA-2)
- [FIPS PUB 180-4 — Secure Hash Standard](https://csrc.nist.gov/pubs/fips/180-4/upd1/final)
