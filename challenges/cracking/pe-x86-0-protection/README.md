# Cracking — PE x86 - 0 protection

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — PE x86 - 0 protection](https://www.root-me.org/en/Challenges/Cracking/PE-x86-0-protection)

El ejecutable PE de 32 bits compara de forma directa la entrada con caracteres constantes; no hay protección anti-análisis relevante.

## Solución

1. Cargar el ejecutable en Ghidra, Cutter o un desensamblador para PE.
2. Buscar las cadenas de éxito/error y seguir sus referencias hasta la función de validación.
3. Reconstruir la secuencia de comparaciones de bytes y usar únicamente el valor final en Root-Me.

El ejecutable oficial sigue disponible, la cuenta ya lo tenía validado y se registró «Like». La respuesta no se publica.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Cracking/PE-x86-0-protection)
- [Ghidra](https://ghidra-sre.org/)
