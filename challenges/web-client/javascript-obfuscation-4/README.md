# Web - Client — Javascript - Obfuscation 4

## Descripción

- **Reto:** [Root-Me — Javascript - Obfuscation 4](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-4)

La lógica de validación se entrega íntegramente en un script de cliente con cadenas codificadas. La ofuscación dificulta la lectura, pero no protege los valores que el navegador recibe.

## Solución

1. Descargar el HTML de la instancia autorizada y aislar su script embebido.
2. Revisar las transformaciones de cadenas usadas por el código, incluidas las decodificaciones Base64 del lado cliente.
3. Distinguir los valores señuelo de la salida usada por el flujo de validación.
4. Enviar únicamente el valor obtenido al formulario de Root-Me.

## Verificación

La solución fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- La ofuscación de JavaScript no sustituye controles de seguridad del lado servidor.
- Los secretos, flags y decisiones de autorización no deben distribuirse al navegador.

