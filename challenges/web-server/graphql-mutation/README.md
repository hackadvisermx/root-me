# Web - Server — GraphQL - Mutation

## Descripción

- **Reto:** [Root-Me — GraphQL - Mutation](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Mutation)

El esquema GraphQL expone una mutación de alta de usuario. Un campo que debería ser definido exclusivamente por el servidor puede incorporarse al `input` de la mutación, permitiendo alterar atributos de la cuenta creada.

## Solución

1. Consultar el esquema de la instancia Start con introspección y localizar las mutaciones, sus tipos de entrada y los campos de salida.
2. Crear una cuenta de prueba mediante la mutación publicada y comparar los atributos aceptados por la interfaz con los del tipo `input`.
3. Añadir al `input` únicamente el atributo no restringido que cambia el privilegio o estado de la cuenta, y solicitar ese atributo en la selección de retorno.
4. Iniciar sesión con la cuenta de prueba resultante y usar el recurso autorizado del reto para obtener el valor de validación.

## Estado de revalidación

La ruta de escalación por *mass assignment* en una mutación GraphQL fue corroborada con material público. Falta reproducirla en la instancia Start autenticada, validar la respuesta y registrar el «Like».

## Notas adicionales

- La autorización debe aplicarse en el resolutor; ocultar un campo en la interfaz no lo protege.
- Los tipos de entrada deben permitir explícitamente solo los atributos modificables por cada rol.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Mutation)
- [GraphQL — Mutations](https://graphql.org/learn/queries/#mutations)
