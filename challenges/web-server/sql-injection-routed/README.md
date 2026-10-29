# Web - Server — SQL Injection - Routed

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — SQL Injection - Routed](https://www.root-me.org/en/Challenges/Web-Server/SQL-Injection-Routed)

El buscador filtra texto visible de una inyección SQL, pero la consulta aún puede recibir expresiones codificadas. La construcción de cadenas mediante representación hexadecimal evita el filtro superficial.

## Solución

1. Localizar el formulario de búsqueda de `index.php?action=search`.
2. Verificar qué palabras o espacios filtra la aplicación y qué expresiones SQL siguen llegando al motor.
3. Codificar las partes filtradas de la carga SQL como literales hexadecimales y reconstruirlas dentro de la consulta, en lugar de enviar directamente el texto bloqueado.
4. Enumerar `information_schema` para confirmar tablas y columnas, y usar el resultado únicamente para validarlo en Root-Me.

## Estado de revalidación

El punto de entrada, la ruta y el bypass mediante literales hexadecimales fueron corroborados con un writeup independiente. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- El filtrado por palabras no sustituye a las consultas preparadas.
- Las capas de enrutamiento no deben transformar entradas sin conservar una separación estricta entre datos y código SQL.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-Injection-Routed)
- [OWASP — SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
