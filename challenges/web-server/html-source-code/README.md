# Web - Server — HTML - Source code

## Descripción

> **Enunciado oficial:** “Don’t search too far”.

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 5
- **Autor:** g0uZ
- **Reto:** [Root-Me — HTML - Source code](https://www.root-me.org/en/Challenges/Web-Server/HTML-Source-code)

El objetivo presenta una página de autenticación muy simple. La pista indica que la respuesta está cerca, por lo que el análisis debe empezar por el documento HTML que recibe el navegador, no por ataques al formulario.

## Solución

1. Iniciar la instancia oficial desde **Start the challenge**.
2. Abrir el código fuente de la página de autenticación con las herramientas de desarrollo del navegador.
3. Revisar los comentarios HTML: uno contiene la contraseña de validación.
4. Introducir esa contraseña en el formulario de la instancia. La página confirma que puede usarse para validar el reto.
5. Enviar el mismo valor al formulario **Enter password** de Root-Me.

La cuenta ya tenía este reto validado; tras repetir el proceso, Root-Me mostró: “Well done but you’ve already won the 5 Points”.

```text
Herramienta principal: inspector / código fuente del navegador.
Lugar relevante: comentario HTML de la página de la instancia.
```

## Notas adicionales

- La contraseña no se incluye en este repositorio.
- Este reto ilustra que los comentarios HTML, aunque no se rendericen, se entregan por completo al cliente y no son un mecanismo de protección.
- La corrección consiste en no guardar secretos en el HTML, JavaScript o cualquier recurso enviado al navegador.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTML-Source-code)
- [MDN — HTML comments](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes#comments)
