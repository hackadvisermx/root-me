# Web - Server — PHP - register globals

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Medium
- **Puntos:** 25
- **Reto:** [Root-Me — PHP - register globals](https://www.root-me.org/en/Challenges/Web-Server/PHP-register-globals)

El código de respaldo muestra que la aplicación confía en `$_SESSION['logged']`. Una configuración vulnerable que promueve parámetros de entrada a variables globales permite inicializar esa estructura desde la query sin una autenticación real.

## Solución

1. Consultar el respaldo `index.php.bak` de la instancia para identificar la condición basada en sesión.
2. Enviar el elemento de sesión desde la query, codificando los corchetes si el cliente lo requiere:

   ```text
   ?_SESSION[logged]=1
   ```

3. La instancia responde con el mensaje de validación.
4. Introducir el dato mostrado solo en Root-Me.

La cuenta ya tenía este reto validado. La sobrescritura de la estructura de sesión mediante la query fue reproducida con una respuesta HTTP 200 y el mensaje de validación.

## Notas adicionales

- `register_globals` fue eliminado de PHP porque mezcla datos no confiables de la petición con variables de la aplicación.
- El estado de autenticación debe ser generado y controlado por el servidor, nunca inicializable desde parámetros HTTP.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-register-globals)
- [PHP — History of register_globals](https://www.php.net/manual/en/security.globals.php)
