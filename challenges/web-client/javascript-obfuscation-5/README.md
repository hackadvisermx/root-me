# Web - Client — Javascript - Obfuscation 5

## Descripción

- **Reto:** [Root-Me — Javascript - Obfuscation 5](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-5)

El reto entrega código cliente con codificación de Microsoft Script Encoder y una comprobación adicional ofuscada. El navegador recibe tanto la transformación como los datos necesarios para reconstruir el valor de validación.

## Solución

1. Descargar los recursos JavaScript de la instancia autorizada.
2. Identificar el bloque codificado con Script Encoder y decodificarlo de manera local para revisión estática.
3. Reconstruir la tabla de sustitución y la comparación que ejecuta el formulario, sin ejecutar contenido fuera de la instancia.
4. Obtener el valor que satisface esa comparación y usarlo únicamente en el formulario oficial de Root-Me.

## Verificación

La solución fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- La ofuscación o codificación de scripts no convierte secretos de cliente en secretos reales.
- Las comprobaciones de autorización deben mantenerse en el servidor.
