# Web - Client — HTML - disabled buttons

## Descripción

- **Categoría:** Web - Client
- **Dificultad:** Easy
- **Puntos:** 5
- **Reto:** [Root-Me — HTML - disabled buttons](https://www.root-me.org/en/Challenges/Web-Client/HTML-disabled-buttons)

El formulario de la instancia parece inaccesible porque sus campos tienen el atributo HTML `disabled`. Esa restricción se aplica únicamente en el navegador y no representa un control de acceso del servidor.

## Solución

1. Abrir la instancia y localizar los controles deshabilitados en el DOM.
2. Eliminar el atributo `disabled` de los campos de texto y envío desde las herramientas de desarrollo, o en la consola:

   ```js
   document.querySelectorAll('[disabled]').forEach((element) => {
     element.removeAttribute('disabled');
   });
   ```

3. Escribir un valor en el campo habilitado y enviar el formulario.
4. Usar el dato devuelto únicamente para la validación en Root-Me.

La cuenta ya tenía este reto validado. Se habilitaron los controles en la instancia oficial y el envío devolvió una respuesta nueva antes de documentarlo.

## Notas adicionales

- `disabled` es una propiedad de la interfaz y se puede cambiar por cualquier usuario con control del navegador.
- La autorización debe verificarse en el servidor, sin basarse en controles ocultos o deshabilitados en HTML.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/HTML-disabled-buttons)
- [MDN — disabled attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/disabled)
