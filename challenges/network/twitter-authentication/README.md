# Network — Twitter authentication

## Descripción

- **Puntos:** 15
- **Reto:** [Root-Me — Twitter authentication](https://www.root-me.org/en/Challenges/Network/Twitter-authentication-101)

El reto proporciona una captura de una autenticación HTTP. La cabecera de autorización contiene datos codificados en Base64, no protegidos criptográficamente.

## Solución

1. Abrir `ch3.pcap` con Wireshark.
2. Filtrar las peticiones con cabecera HTTP de autorización:

   ```text
   http.authorization
   ```

3. Extraer el valor Basic y decodificarlo localmente con Base64.
4. Introducir el dato recuperado solo en Root-Me.

La captura oficial fue revisada y contiene una cabecera de autorización HTTP. El «Like» quedó registrado en la página del reto.

## Notas adicionales

- Las credenciales en Basic Auth son recuperables por cualquier observador de tráfico no cifrado.
- El nombre histórico del reto no debe confundirse con una evaluación de servicios reales de terceros.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Network/Twitter-authentication-101)
- [RFC 7617 — HTTP Basic Authentication](https://www.rfc-editor.org/rfc/rfc7617)
