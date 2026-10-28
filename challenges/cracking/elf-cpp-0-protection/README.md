# Cracking — ELF C++ - 0 protection

## Descripción

- **Puntos:** 10
- **Reto:** [Root-Me — ELF C++ - 0 protection](https://www.root-me.org/en/Challenges/Cracking/ELF-C-0-protection)

El binario C++ construye el valor de validación en una función auxiliar. Aunque los símbolos y objetos C++ hacen el flujo menos directo, no implementa protección anti-reversing.

## Solución

1. Abrir `ch25.bin` en Ghidra o GDB y localizar la rutina que prepara el valor de comparación.
2. Seguir la función auxiliar y observar su valor de retorno o su búfer después de ejecutarse dentro de un entorno aislado.
3. Reconstruir el texto resultante y validarlo exclusivamente en Root-Me.

El recurso oficial y la resolución histórica de la cuenta fueron comprobados; el «Like» quedó registrado. No se incluye el valor de validación.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cracking/ELF-C-0-protection)
- [GDB documentation](https://sourceware.org/gdb/documentation/)
