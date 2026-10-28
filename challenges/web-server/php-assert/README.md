# Web - Server — PHP - assert()

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Medium
- **Puntos:** 25
- **Reto:** [Root-Me — PHP - assert()](https://www.root-me.org/en/Challenges/Web-Server/PHP-assert)

La aplicación concatena el parámetro `page` dentro de una condición enviada a `assert()`. En versiones antiguas de PHP, una aserción de cadena se evalúa como código, de modo que una comilla controlada permite escapar de la expresión de validación.

## Solución

1. Probar una ruta inexistente para observar que la aplicación construye nombres bajo `includes/` y añade `.php`.
2. Probar `..` para confirmar que la condición de bloqueo se implementa con `assert()`.
3. Cerrar la cadena usada por la aserción, ejecutar una expresión de lectura dentro de la instancia y reabrir la llamada de comprobación. El patrón reproducido es:

   ```text
   ','exp') || print_r(file_get_contents(".passwd")) || strpos('
   ```

4. Codificar el valor como parámetro `page`; la salida de la aserción aparece antes del posterior mensaje de archivo inexistente.
5. Usar el dato recuperado solo en Root-Me.

La cuenta ya tenía este reto validado. Se confirmó que el payload introduce salida nueva y que la aplicación continúa con su comprobación de archivo después de evaluarlo.

## Notas adicionales

- El comportamiento de evaluar cadenas con `assert()` quedó obsoleto y fue eliminado en PHP moderno; nunca se deben construir expresiones ejecutables con entradas de usuario.
- La validación debe partir de una lista de páginas permitidas, no de una expresión dinámica.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-assert)
- [PHP — assert](https://www.php.net/manual/en/function.assert.php)
