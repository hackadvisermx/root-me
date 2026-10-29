# Web - Server — Node - Serialize

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — Node - Serialize](https://www.root-me.org/en/Challenges/Web-Server/Node-Serialize)

La aplicación serializa el perfil de usuario en una cookie y lo deserializa con una biblioteca vulnerable de Node.js. Los valores especiales que representan funciones se ejecutan al deserializarse.

## Solución

1. Iniciar sesión con una cuenta de prueba y decodificar la cookie `profile` para identificar el objeto serializado.
2. Reemplazar un atributo controlable por una función serializada inmediatamente invocada, usando el formato reconocido por la biblioteca vulnerable.
3. Empezar con una comprobación inocua que confirme evaluación y, solo dentro de la instancia CTF, usar las APIs de archivos del proceso para localizar el recurso objetivo indicado por el reto.
4. Volver a codificar la cookie y enviarla a la aplicación; usar el resultado únicamente para Root-Me.

## Estado de revalidación

El formato de la cookie y la deserialización insegura fueron corroborados mediante un análisis público del reto. Falta reproducirlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Nunca deserializar datos controlados por el cliente como objetos ejecutables.
- Las sesiones deben usar identificadores aleatorios del lado del servidor, no perfiles serializados en el cliente.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Node-Serialize)
- [CVE-2017-5941](https://nvd.nist.gov/vuln/detail/CVE-2017-5941)
