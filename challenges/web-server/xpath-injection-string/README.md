# Web - Server — XPath injection - String

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — XPath injection - String](https://www.root-me.org/en/Challenges/Web-Server/XPath-injection-String)

La aplicación concatena un valor de búsqueda en una expresión XPath que devuelve texto. El resultado visible permite convertir una inyección booleana en extracción progresiva de una cadena.

## Solución

1. Localizar el campo de búsqueda y comprobar que comillas o predicados alteran la respuesta XPath.
2. Cerrar el literal del predicado y añadir una condición que distinga entre verdadero y falso.
3. Obtener la longitud y cada carácter del texto objetivo con predicados XPath, registrando solo los resultados necesarios para el reto.
4. Validar el valor reconstruido en Root-Me y registrar el «Like».

## Estado de revalidación

La extracción de texto mediante predicados XPath fue corroborada con material público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las consultas XPath deben recibir variables enlazadas o usar una API que impida construir la expresión por concatenación.
- Escapar texto no sustituye una separación correcta entre código XPath y datos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XPath-injection-String)
- [OWASP — XPath Injection](https://owasp.org/www-community/attacks/XPATH_Injection)
