# Web - Server — PHP - preg_replace()

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — PHP - preg_replace()](https://www.root-me.org/en/Challenges/Web-Server/PHP-preg-replace)

El patrón regular controlado por el usuario permite activar el modificador heredado `/e` de `preg_replace`. En versiones vulnerables, dicho modificador evalúa el reemplazo como PHP cuando el patrón coincide.

## Solución

1. Enviar el formulario `POST` con los parámetros `search`, `replace` y `content`.
2. Confirmar primero la evaluación con una expresión inocua que produzca un valor conocido:

   ```text
   search  = /probe/e
   replace = md5('preg-evidence')
   content = probe
   ```

3. Tras confirmar que la coincidencia evalúa `replace`, sustituir la prueba por una lectura del recurso objetivo indicado por el reto.
4. Usar el resultado exclusivamente para validarlo en Root-Me.

## Estado de revalidación

La ruta, parámetros y condición de coincidencia fueron contrastados con documentación independiente. Falta ejecutar la reproducción en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- El modificador `/e` fue eliminado de PHP; nunca debe usarse en código heredado.
- Separar el patrón del contenido no elimina el riesgo si ambos siguen bajo control del usuario.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-preg-replace)
- [PHP — preg_replace](https://www.php.net/manual/en/function.preg-replace.php)
