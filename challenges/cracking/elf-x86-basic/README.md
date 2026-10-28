# Cracking — ELF x86 - Basic

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — ELF x86 - Basic](https://www.root-me.org/en/Challenges/Cracking/ELF-x86-Basic)

El binario solicita campos consecutivos y compara cada uno mediante ramas condicionales x86.

## Solución

1. Analizar el binario en una VM Linux de 32 bits con GDB o decompilarlo.
2. Localizar las llamadas a comparación de cadenas y las instrucciones `jne` posteriores.
3. Leer las cadenas esperadas o, con fines de análisis, detenerse antes de cada salto y observar el flujo que lleva al mensaje de éxito.
4. Usar la respuesta solamente en Root-Me.

El recurso oficial y la resolución previa de la cuenta fueron verificados; el «Like» quedó registrado.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cracking/ELF-x86-Basic)
- [GDB documentation](https://sourceware.org/gdb/documentation/)
