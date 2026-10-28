# Web - Client — XSS - Stored 1

## Descripción

- **Dificultad:** Hard
- **Puntos:** 30
- **Reto:** [Root-Me — XSS - Stored 1](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-1)

La aplicación persiste una entrada controlada por usuario y la vuelve a insertar en HTML sin codificación contextual. El navegador de una visita posterior interpreta el contenido como código.

## Solución

1. Identificar el campo que se almacena y la vista donde se vuelve a mostrar.
2. En la instancia aislada, comprobar la interpretación con una prueba mínima e inocua:

   ```html
   <script>alert(1)</script>
   ```

3. Adaptar el análisis al flujo del reto para obtener el dato de validación, sin enviarlo ni guardar información de terceros.
4. Introducirlo únicamente en Root-Me.

## Estado de revalidación

La cuenta conserva el reto validado y recibió «Like». La instancia histórica no está disponible con el flujo original, así que el writeup conserva la técnica retroactiva y no publica ninguna respuesta.

## Notas adicionales

- Toda salida HTML debe codificarse según el contexto; los filtros de listas negras no son suficientes.
- Una política CSP defensiva ayuda, pero no reemplaza el encoding correcto.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-1)
- [OWASP Cross Site Scripting Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
