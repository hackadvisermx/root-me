# Cryptanalysis — Encoding - ASCII

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — Encoding - ASCII](https://www.root-me.org/en/Challenges/Cryptanalysis/Encoding-ASCII)

El reto presenta valores numéricos que representan códigos ASCII. Es codificación, no cifrado.

## Solución

1. Separar los valores decimales u octales indicados por el reto.
2. Convertir cada valor al carácter ASCII correspondiente:

   ```python
   ''.join(chr(value) for value in values)
   ```

3. Usar el texto resultante solo en Root-Me.

La cuenta mantiene el reto validado y se registró «Like». La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cryptanalysis/Encoding-ASCII)
- [ASCII table](https://www.asciitable.com/)
