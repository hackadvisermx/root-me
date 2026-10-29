# Web - Server — Local File Inclusion - Wrappers

## Descripción

- **Reto:** [Root-Me — Local File Inclusion - Wrappers](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion-Wrappers)

Un parámetro de inclusión local acepta *wrappers* de PHP. La carga de una imagen permite alojar un contenedor ZIP y el wrapper `zip://` hace que PHP procese un archivo interno controlado por el usuario.

## Solución

1. Confirmar que el parámetro de página concatena o incluye un nombre de archivo y que el flujo de carga acepta una imagen de prueba.
2. Crear localmente un ZIP con un archivo PHP de diagnóstico inocuo, renombrar el contenedor con la extensión admitida y cargarlo en la instancia Start.
3. Referenciar el archivo interno con el wrapper `zip://`; el separador interno se codifica como `%23` cuando forma parte del parámetro de consulta.
4. Una vez demostrada la inclusión, limitar la lectura al recurso objetivo indicado por el reto y enviar el resultado solamente a Root-Me para validación.

## Estado de revalidación

El patrón de inclusión mediante `zip://` y un archivo ZIP renombrado fue corroborado con un writeup público. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Los nombres de archivo controlados por usuario nunca deben llegar a `include`, `require` o wrappers de PHP.
- Aplicar una lista cerrada de vistas y almacenar las cargas fuera de rutas interpretables por PHP.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion-Wrappers)
- [PHP — Supported Protocols and Wrappers](https://www.php.net/wrappers)
