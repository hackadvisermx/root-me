# Web - Server — File upload - Polyglot

## Descripción

- **Puntos:** 45
- **Reto:** [Root-Me — File upload - Polyglot](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Polyglot)

El control de carga acepta archivos que superan una comprobación superficial de imagen. Un archivo políglota puede ser válido como imagen y contener una segunda estructura interpretada posteriormente por el servidor.

## Solución

1. Revisar el flujo de carga y determinar si valida extensión, MIME, bytes mágicos o una combinación incompleta de ellos.
2. Construir localmente un archivo políglota mínimo con una cabecera de imagen válida y una segunda estructura apta para el flujo del reto; empezar con metadatos inocuos.
3. Cargarlo en la instancia Start y comprobar cómo lo procesa la aplicación sin ejecutar acciones fuera del entorno CTF.
4. Usar el comportamiento resultante solo para obtener el dato objetivo y validarlo en Root-Me.

## Estado de revalidación

El vector de archivo políglota para sortear una validación superficial fue corroborado con writeups públicos. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Validar el contenido con un decodificador real, re-encodarlo del lado servidor y conservar cargas fuera del directorio ejecutable.
- No deserializar metadatos ni abrir cargas mediante wrappers interpretables.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/File-upload-Polyglot)
- [OWASP — File Upload Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html)
