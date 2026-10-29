# Web - Server — XPath injection - Authentication

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — XPath injection - Authentication](https://www.root-me.org/en/Challenges/Web-Server/XPath-injection-Authentication)

El formulario concatena usuario y contraseña dentro de un predicado XPath. Una condición booleana controlada por el usuario convierte la autenticación en una consulta que coincide con una entrada existente.

## Solución

1. Confirmar el contexto XPath con un carácter de comilla que produzca un error de sintaxis controlado.
2. Cerrar el literal del nombre de usuario e introducir una condición verdadera en el predicado.
3. Completar o neutralizar la expresión restante según las comillas que utilice el formulario, conservando una estructura XPath válida.
4. Usar los atributos devueltos por la entrada autenticada exclusivamente para la validación de Root-Me.

## Estado de revalidación

El vector se documentó a nivel de técnica. Falta reproducir el predicado exacto en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las consultas XPath deben usar variables enlazadas o escapes contextuales robustos; no concatenar expresiones con entradas de usuario.
- Evitar mensajes de error que revelen la estructura XML o XPath.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XPath-injection-Authentication)
- [OWASP — XPath Injection](https://owasp.org/www-community/attacks/XPATH_Injection)
