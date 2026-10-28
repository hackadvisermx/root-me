# Cracking — ELF x86 - 0 protection

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — ELF x86 - 0 protection](https://www.root-me.org/en/Challenges/Cracking/ELF-x86-0-protection)

El binario ELF de 32 bits no incluye protecciones ni ofuscación. La comparación de la entrada es visible mediante análisis estático.

## Solución

1. Descargar y descomprimir el recurso oficial.
2. Identificar formato y arquitectura:

   ```bash
   file ch1.bin
   ```

3. Abrirlo con Ghidra, Cutter o GDB y seguir la función que compara la entrada con la cadena esperada.
4. Validar solo el valor obtenido en Root-Me.

La cuenta conserva el reto resuelto, el recurso oficial sigue disponible y el «Like» fue registrado. No se versiona la respuesta.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cracking/ELF-x86-0-protection)
- [Ghidra](https://ghidra-sre.org/)
