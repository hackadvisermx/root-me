# Web - Server — Elixir - EEx

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — Elixir - EEx](https://www.root-me.org/en/Challenges/Web-Server/Elixir-EEx)

El contenido controlado por el usuario se evalúa como una plantilla EEx. Las etiquetas `<%= ... %>` ejecutan expresiones Elixir y renderizan su resultado, convirtiendo una plantilla no confiable en SSTI.

## Solución

1. Confirmar la evaluación con una expresión aritmética inocua:

   ```eex
   <%= 7 * 7 %>
   ```

2. Tras confirmar el contexto EEx, usar una función de lectura de archivos en la plantilla para acceder únicamente al recurso objetivo indicado por el reto:

   ```eex
   <%= File.read!("/ruta-indicada-por-el-reto") %>
   ```

3. Usar el resultado exclusivamente para validarlo en Root-Me.

## Estado de revalidación

La semántica de EEx y el vector SSTI fueron contrastados con la documentación oficial de Elixir. Falta iniciar la instancia Start autenticada, localizar el campo vulnerable, reproducir la lectura, validar y registrar el «Like».

## Notas adicionales

- EEx no debe evaluar plantillas que contengan entrada no confiable; los valores se deben pasar como datos a una plantilla fija.
- El proceso de generación debe tener permisos mínimos y sin acceso a secretos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Elixir-EEx)
- [Elixir — EEx](https://hexdocs.pm/eex/EEx.html)
