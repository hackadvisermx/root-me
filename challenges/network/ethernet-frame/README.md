# Network — ETHERNET - frame

## Descripción

- **Puntos:** 10
- **Reto:** [Root-Me — ETHERNET - frame](https://www.root-me.org/en/Challenges/Network/ETHERNET-frame)

El recurso presenta un volcado hexadecimal de una trama Ethernet que encapsula IPv6, TCP y una petición HTTP. Los datos confidenciales aparecen en una cabecera HTTP Basic.

## Solución

1. Convertir el volcado hexadecimal a bytes y localizar la carga HTTP tras las cabeceras Ethernet, IPv6 y TCP.
2. Identificar la cabecera `Authorization: Basic` en la petición HTTP.
3. Decodificar únicamente su valor Base64:

   ```bash
   printf '%s' '<valor-base64>' | base64 -d
   ```

4. Usar el resultado únicamente para validar el reto en Root-Me.

El volcado oficial se analizó de nuevo: contiene la cabecera HTTP Basic y el valor se decodifica correctamente. El «Like» quedó registrado.

## Notas adicionales

- Basic Authentication solo codifica en Base64; no cifra las credenciales.
- La autenticación HTTP debe emplearse sobre TLS y con controles de servidor apropiados.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Network/ETHERNET-frame)
- [RFC 7617 — HTTP Basic Authentication](https://www.rfc-editor.org/rfc/rfc7617)
