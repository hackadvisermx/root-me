# Web - Server — Yaml - Deserialization

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — Yaml - Deserialization](https://www.root-me.org/en/Challenges/Web-Server/Yaml-Deserialization)

La aplicación decodifica Base64 desde la ruta y deserializa el contenido con un cargador YAML inseguro de Python. Las etiquetas Python permiten invocar procesos durante la deserialización.

## Solución

1. Decodificar el segmento Base64 inicial para confirmar que se interpreta como YAML.
2. Sustituir el mensaje por una etiqueta Python que ejecute primero una comprobación inocua en la instancia CTF.
3. Codificar de nuevo el YAML y enviarlo como segmento de ruta. El formato vulnerable es equivalente a:

   ```yaml
   yaml: !!python/object/new:subprocess.check_output [["comando", "de-prueba"]]
   ```

4. Usar el mismo mecanismo únicamente para leer el recurso objetivo indicado por el reto y validar el resultado en Root-Me.

## Estado de revalidación

La ruta Base64 y el uso de `subprocess.check_output` fueron corroborados con un análisis público. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Usar `yaml.safe_load()` o un cargador con lista cerrada de tipos; nunca deserializar etiquetas de objetos desde una ruta controlada por usuario.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Yaml-Deserialization)
- [PyYAML — safe_load](https://pyyaml.org/wiki/PyYAMLDocumentation)
