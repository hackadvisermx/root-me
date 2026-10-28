# Cryptanalysis — Encoding - UU

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — Encoding - UU](https://www.root-me.org/en/Challenges/Cryptanalysis/Encoding-UU)

El texto está codificado con uuencode, un formato histórico de transporte de datos.

## Solución

1. Guardar el bloque uuencode incluyendo sus líneas de inicio y fin cuando existan.
2. Decodificarlo localmente:

   ```bash
   uudecode < mensaje.uu
   ```

3. Leer el contenido resultante y validarlo solo en Root-Me.

La cuenta ya tenía el reto resuelto y se registró «Like». No se publica la respuesta.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cryptanalysis/Encoding-UU)
- [uuencode specification](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/uudecode.html)
