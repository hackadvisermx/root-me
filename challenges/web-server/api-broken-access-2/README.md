# Web - Server — API - Broken Access 2

## Descripción

- **Puntos:** 40
- **Reto:** [Root-Me — API - Broken Access 2](https://www.root-me.org/en/Challenges/Web-Server/API-Broken-Access-2)

El recurso de perfil confía en un identificador UUID de versión 1 predecible. La instancia expone los parámetros temporales y de nodo necesarios para reconstruir el UUID asociado al perfil que contiene el dato de validación.

## Solución

1. Examinar el perfil de prueba y reunir la marca temporal, identificador de nodo y secuencia que el reto expone.
2. Convertir la fecha al número de intervalos de 100 ns desde la época UUID (15 de octubre de 1582).
3. Reconstruir el UUID v1 con esos componentes y solicitar el perfil con el identificador derivado.
4. Usar el valor de la nota devuelta exclusivamente para validarlo en Root-Me.

## Verificación

La reconstrucción del UUID fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- Los identificadores no son mecanismos de autorización. Cada recurso debe comprobar propiedad y permisos del solicitante.
- Evitar exponer metadatos que permitan predecir identificadores emitidos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/API-Broken-Access-2)
- [RFC 4122 — UUID](https://www.rfc-editor.org/rfc/rfc4122)
