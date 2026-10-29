# Web - Server — HTTP - IP restriction bypass

## Descripción

> **Enunciado oficial:** “Only local users will be able to access the page.”

- **Categoría:** Web - Server
- **Puntos:** 10
- **Reto:** [Root-Me — HTTP - IP restriction bypass](https://www.root-me.org/en/Challenges/Web-Server/HTTP-IP-restriction-bypass)

La instancia concede acceso si cree que el cliente tiene una dirección privada. Confía indebidamente en una cabecera HTTP que el usuario puede suministrar.

## Solución

1. Solicitar la página sin cabeceras adicionales y confirmar que deniega el acceso externo.
2. Repetir la petición declarando una dirección privada mediante `X-Forwarded-For`:

   ```bash
   curl -H 'X-Forwarded-For: 192.168.1.1' \
     http://challenge01.root-me.org/web-serveur/ch68/
   ```

3. La instancia devuelve el dato de validación. Introducirlo únicamente en Root-Me.

La respuesta fue validada en Root-Me y el reto ahora muestra palomita en el catálogo. El «Like» también quedó registrado.

## Notas adicionales

- `X-Forwarded-For` solo es confiable si un proxy controlado lo elimina de peticiones externas y lo añade él mismo.
- La autorización por red debe basarse en la dirección observada por infraestructura confiable, no en una cabecera directa del cliente.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-IP-restriction-bypass)
- [RFC 1918 — Address Allocation for Private Internets](https://www.rfc-editor.org/rfc/rfc1918)
