# Web - Server — Ruby on Rails - ransack

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — Ruby on Rails - ransack](https://www.root-me.org/en/Challenges/Web-Server/Ruby-on-Rails-ransack)

El filtro avanzado Ransack permite buscar atributos no previstos siempre que el predicado termine en `_cont`. Esto convierte la búsqueda sobre `password_digest` en un oráculo de subcadenas.

## Solución

1. Identificar al usuario administrador mediante atributos que la lista pública expone.
2. Anclar la búsqueda a ese usuario con un atributo permitido, por ejemplo:

   ```text
   q[first_name_cont]=<administrador>
   ```

3. Añadir un candidato de subcadena para el digest:

   ```text
   q[password_digest_cont]=<candidato>
   ```

4. Interpretar el resultado: una coincidencia confirma que el digest contiene el candidato; ninguna coincidencia lo descarta.
5. Extender la subcadena hexadecimal carácter por carácter hasta reconstruir el digest y verificarlo fuera de línea antes de usar la contraseña únicamente en la instancia del reto.

## Estado de revalidación

La ruta de búsqueda y el oráculo de subcadenas se verificaron por análisis. Falta ejecutarlo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- La autorización debe limitar atributos y predicados, no solo el sufijo de un parámetro.
- Los digests de contraseña nunca deben poder filtrarse o consultarse desde formularios de búsqueda.
- La respuesta y el digest no se versionan.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Ruby-on-Rails-ransack)
- [Ransack — documentation](https://activerecord-hackery.github.io/ransack/)
