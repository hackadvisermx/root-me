# Web - Server — PHP - Eval - Advanced filters bypass

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — PHP - Eval - Advanced filters bypass](https://www.root-me.org/en/Challenges/Web-Server/PHP-Eval-Advanced-filters-bypass)

El reto aumenta los filtros sobre el código enviado a `eval`, pero conserva el error de diseño: se permite que la entrada controle una expresión interpretada por PHP.

## Solución

1. Inventariar con precisión los caracteres y patrones que rechaza el filtro de la instancia Start.
2. Validar con una expresión sin efectos que los operadores permitidos siguen siendo evaluados por PHP.
3. Generar los caracteres necesarios mediante operaciones entre literales admitidos y concatenarlos para formar el nombre dinámico de una función.
4. Ejecutar una comprobación inocua antes de limitar la lectura al recurso objetivo del reto y validar el resultado exclusivamente en Root-Me.

## Estado de revalidación

La técnica de construir identificadores en tiempo de ejecución para sortear una lista negra fue corroborada con un writeup público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Los filtros léxicos no son una frontera de seguridad para un intérprete de código.
- Eliminar la evaluación y diseñar una gramática limitada para las operaciones que realmente se necesitan.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Eval-Advanced-filters-bypass)
- [OWASP — Code Injection](https://owasp.org/www-community/attacks/Code_Injection)
