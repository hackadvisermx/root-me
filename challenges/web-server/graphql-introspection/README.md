# Web - Server — GraphQL - Introspection

## Descripción

- **Puntos:** 20
- **Reto:** [Root-Me — GraphQL - Introspection](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Introspection)

La introspección habilitada expone el esquema GraphQL, incluidos una consulta no publicada y el campo que devuelve el resultado del reto.

## Solución

1. Consultar el endpoint GraphQL con una consulta de introspección limitada para enumerar tipos, campos y argumentos.
2. Identificar la operación `IAmNotHere`, que requiere el argumento entero `very_long_id`.
3. Solicitar únicamente el campo no sensible necesario:

   ```graphql
   { IAmNotHere(very_long_id: 17) { very_long_value } }
   ```

4. Usar el valor devuelto exclusivamente para la validación en Root-Me.

## Estado de revalidación

La técnica y la respuesta de la instancia se comprobaron en segundo plano. Falta enviar la respuesta autenticada y registrar el «Like» en Root-Me; hasta entonces no se cuenta como validado.

## Notas adicionales

- En producción debe deshabilitarse o restringirse la introspección a personal autorizado.
- El esquema no debe revelar operaciones administrativas ni nombres de datos sensibles.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Introspection)
- [GraphQL — Introspection](https://graphql.org/learn/introspection/)
