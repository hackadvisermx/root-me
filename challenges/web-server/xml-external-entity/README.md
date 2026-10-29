# Web - Server — XML External Entity

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — XML External Entity](https://www.root-me.org/en/Challenges/Web-Server/XML-External-Entity)

El procesador XML de la instancia acepta una declaración `DOCTYPE` y resuelve entidades externas. Una entidad local incluida en un campo que la respuesta refleja permite leer el recurso objetivo del reto.

## Solución

1. Identificar la estructura XML esperada y mantener su elemento raíz.
2. Añadir una entidad externa local apuntando solo al recurso indicado en el enunciado:

   ```xml
   <!DOCTYPE root [<!ENTITY xxe SYSTEM "file:///ruta-indicada">]>
   ```

3. Referenciar `&xxe;` dentro de un campo que la aplicación devuelva o procese.
4. Usar el contenido resultante exclusivamente para la validación en Root-Me.

## Estado de revalidación

La superficie XXE se documentó a partir de la categoría y la guía de pruebas de Root-Me. Falta construir el XML exacto para la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Los analizadores XML deben deshabilitar DTDs y entidades externas.
- Procesar XML con permisos mínimos y sin acceso a recursos de red o archivos no requeridos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XML-External-Entity)
- [OWASP — XXE Prevention](https://cheatsheetseries.owasp.org/cheatsheets/XML_External_Entity_Prevention_Cheat_Sheet.html)
