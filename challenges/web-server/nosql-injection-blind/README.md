# Web - Server — NoSQL injection - Blind

## Descripción

- **Puntos:** 45
- **Reto:** [Root-Me — NoSQL injection - blind](https://www.root-me.org/en/Challenges/Web-Server/NoSQL-injection-blind)

La aplicación transforma datos de autenticación controlados por el usuario en un filtro NoSQL. No muestra el documento resultante, pero sí ofrece una diferencia observable entre una condición verdadera y una falsa.

## Solución

1. Capturar una autenticación normal y comprobar cómo el servidor interpreta valores escalares y objetos JSON en los campos recibidos.
2. Formular una condición booleana inocua que produzca dos respuestas distinguibles, sin enumerar cuentas ajenas al reto.
3. Usar operadores del motor NoSQL para inferir longitud y caracteres del dato objetivo por prefijos, guardando el resultado de cada comprobación.
4. Reconstruir solo el valor indicado por el reto, validarlo en Root-Me y registrar el «Like».

## Estado de revalidación

La extracción ciega mediante operadores de consulta NoSQL fue corroborada con material público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Validar tipos y esquema de entrada; los campos de autenticación deben aceptar cadenas, no objetos de consulta.
- No trasladar objetos del cliente directamente a filtros del motor de datos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/NoSQL-injection-blind)
- [OWASP — NoSQL Injection](https://owasp.org/www-community/attacks/NoSQL_Injection)
