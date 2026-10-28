# App - Script — Bash - System 1

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — Bash - System 1](https://www.root-me.org/en/Challenges/App-Script/Bash-System-1)

La instancia SSH contiene un binario SUID cuyo código llama a `system("ls …")` con un nombre de comando relativo. El proceso hereda `PATH`, de modo que puede ejecutar un `ls` controlado antes que el binario del sistema.

## Solución

1. Conectarse solo con las credenciales y host proporcionados por el enunciado de Root-Me.
2. Revisar el código fuente del binario para confirmar `system()` con `ls` sin ruta absoluta.
3. En un directorio escribible de la instancia, crear un ejecutable llamado `ls` que realice la lectura requerida por el reto.
4. Anteponer ese directorio a `PATH` y ejecutar el binario SUID.
5. Usar el resultado exclusivamente en Root-Me.

La cuenta ya tenía el reto validado y se registró «Like». No se incluyen credenciales SSH, rutas sensibles ni la respuesta.

## Notas adicionales

- Un binario privilegiado no debe invocar una shell ni resolver comandos por `PATH`.
- Usar rutas absolutas y `execve` con un entorno controlado reduce esta superficie de ataque.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/App-Script/Bash-System-1)
- [OWASP — OS Command Injection Defense Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/OS_Command_Injection_Defense_Cheat_Sheet.html)
