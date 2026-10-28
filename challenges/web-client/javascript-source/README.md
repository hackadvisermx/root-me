# Web - Client — Javascript - Source

## Descripción

- **Dificultad:** Easy
- **Puntos:** 5
- **Reto:** [Root-Me — Javascript - Source](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Source)

El reto pide un valor mediante una ventana de JavaScript, pero el propio recurso cliente contiene el valor y la lógica de comparación.

## Solución

1. Inspeccionar las etiquetas `<script>` y los recursos cargados por la página.
2. Revisar la respuesta de red que contiene la variable o comparación de contraseña; evitar una respuesta `304` desde caché deshabilitando caché en DevTools si fuera necesario.
3. Introducir el valor recuperado únicamente en Root-Me.

## Estado de revalidación

La cuenta conserva la validación y el «Like» fue registrado. La instancia antigua ya no devuelve el recurso original, por lo que el proceso se reconstruyó con el flujo histórico documentado, sin versionar la respuesta.

## Notas adicionales

- El código y los recursos descargados por el navegador no son secretos.
- Las decisiones de acceso requieren una comprobación de servidor.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Source)
- [MDN — HTTP 304 Not Modified](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/304)
