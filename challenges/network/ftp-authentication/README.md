# Network — FTP - authentication

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — FTP - authentication](https://www.root-me.org/en/Challenges/Network/FTP-Authentication)

El recurso es una captura PCAP de un intercambio FTP autenticado. FTP clásico envía los comandos de usuario y contraseña sin cifrado.

## Solución

1. Descargar el PCAP oficial y abrirlo en Wireshark.
2. Aplicar el filtro de visualización `ftp` o filtrar los comandos `USER` y `PASS`.
3. Leer el argumento del comando `PASS` y usarlo únicamente para validar en Root-Me.

También puede revisarse en terminal:

```bash
tshark -r ch1.pcap -Y 'ftp.request.command == "USER" || ftp.request.command == "PASS"' \
  -T fields -e ftp.request.command -e ftp.request.arg
```

La captura oficial fue analizada de nuevo y contiene los comandos de autenticación en texto claro. El «Like» quedó registrado en Root-Me.

## Notas adicionales

- FTP sin TLS expone credenciales a quien capture la red.
- Usar FTPS o SFTP y evitar protocolos de autenticación sin cifrado.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Network/FTP-Authentication)
- [RFC 959 — File Transfer Protocol](https://www.rfc-editor.org/rfc/rfc959)
