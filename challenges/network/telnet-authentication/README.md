# Network — TELNET - authentication

## Descripción

- **Puntos:** 5
- **Reto:** [Root-Me — TELNET - authentication](https://www.root-me.org/en/Challenges/Network/TELNET-Authentication)

La captura contiene una sesión Telnet. El protocolo transmite la interacción de terminal sin confidencialidad, incluidos los caracteres escritos durante el inicio de sesión.

## Solución

1. Abrir `ch2.pcap` en Wireshark.
2. Aplicar `telnet` como filtro y usar **Follow TCP Stream** en la sesión correspondiente.
3. Reconstruir los caracteres posteriores al prompt de contraseña y validarlos solo en Root-Me.

En terminal, puede identificarse el tráfico con:

```bash
tshark -r ch2.pcap -Y telnet -T fields -e telnet.data
```

La captura oficial se revisó y contiene tráfico Telnet aplicable. El «Like» quedó registrado.

## Notas adicionales

- Telnet no protege la confidencialidad ni la integridad de una sesión.
- Debe sustituirse por SSH.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Network/TELNET-Authentication)
- [RFC 854 — Telnet Protocol Specification](https://www.rfc-editor.org/rfc/rfc854)
