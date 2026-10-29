# Web - Server — PHP - Eval

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — PHP - Eval](https://www.root-me.org/en/Challenges/Web-Server/PHP-Eval)

La aplicación evalúa una expresión PHP procedente de la petición. Un filtro basado en una lista negra intenta impedir llamadas peligrosas, pero la expresión sigue siendo controlada por el usuario.

## Solución

1. Revisar el código fuente que expone el reto para identificar la expresión evaluada y los caracteres bloqueados.
2. Confirmar la evaluación con una operación PHP inocua que no dependa de datos externos.
3. Construir las cadenas requeridas en tiempo de ejecución, sin incluir directamente los identificadores filtrados, y usarlas como nombre de función dinámico.
4. Aplicar el mismo mecanismo solo al recurso de validación de la instancia Start y enviar el resultado a Root-Me.

## Estado de revalidación

La evaluación insegura y la construcción dinámica de cadenas fueron corroboradas con un writeup público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- `eval()` no debe procesar entrada de usuarios; una lista negra no convierte código en datos.
- Sustituir expresiones dinámicas por un conjunto cerrado de operaciones implementadas sin evaluación.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Eval)
- [PHP — eval](https://www.php.net/manual/en/function.eval.php)
