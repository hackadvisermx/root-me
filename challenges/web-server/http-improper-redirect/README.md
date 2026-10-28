# Web - Server — HTTP - Improper redirect

## Descripción

> **Enunciado oficial:** “Get access to index.”

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — HTTP - Improper redirect](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Improper-redirect)

La ruta protegida responde con una redirección HTTP, pero el programa no termina su ejecución. Por ello, el cuerpo de la misma respuesta de redirección contiene información que el navegador normalmente oculta al seguir `Location` de forma automática.

## Solución

1. Solicitar directamente el recurso de índice y evitar seguir redirecciones:

   ```bash
   curl -i --max-redirs 0 \\
     http://challenge01.root-me.org/web-serveur/ch32/index.php
   ```

2. Confirmar que la respuesta tiene un estado `3xx` y conservar su cuerpo.
3. Leer el dato de validación presente en ese cuerpo, sin permitir que el cliente cambie a la página de inicio de sesión.
4. Introducirlo únicamente en Root-Me.

La cuenta ya tenía este reto validado. La instancia volvió a entregar el cuerpo junto a la redirección al repetir el proceso.

## Notas adicionales

- Una redirección HTTP no detiene por sí sola la ejecución de una aplicación.
- En PHP, después de emitir `Location`, el flujo debe finalizar explícitamente, por ejemplo con `exit`.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Improper-redirect)
- [PHP — header](https://www.php.net/manual/en/function.header.php)
