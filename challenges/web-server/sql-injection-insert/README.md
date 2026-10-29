# Web - Server — SQL injection - Insert

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — SQL injection - Insert](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Insert)

El flujo de registro concatena campos controlados por el usuario en una sentencia `INSERT`. La aplicación permite introducir valores que modifican la fila creada en vez de tratarlos como datos.

## Solución

1. Registrar una cuenta de prueba y observar qué atributos se guardan y se muestran después de autenticar.
2. Enviar variaciones controladas en cada campo de alta para identificar cuál se inserta sin parametrización.
3. Ajustar la sintaxis al contexto de `VALUES` y verificar con una cuenta desechable que la fila resultante contiene el atributo esperado.
4. Usar el efecto de esa inserción solo para alcanzar el recurso autorizado del reto y validar el valor en Root-Me.

## Estado de revalidación

La inyección en el formulario de alta y el contexto `INSERT` fueron corroborados con un writeup público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Todas las sentencias `INSERT` deben usar parámetros enlazados, incluidos los campos opcionales.
- La cuenta de base de datos debe tener el mínimo privilegio requerido.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Insert)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
