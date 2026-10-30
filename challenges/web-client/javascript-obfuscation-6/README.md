# Web - Client — Javascript - Obfuscation 6

## Descripción

- **Reto:** [Root-Me — Javascript - Obfuscation 6](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-6)

La instancia simula un reproductor que recibe una dirección cifrada. La lógica de descifrado, el material usado para derivar su clave y el resultado se distribuyen al cliente en JavaScript ofuscado.

## Solución

1. Revisar los scripts estáticos de la instancia y aislar la rutina de descifrado.
2. Reproducir localmente el flujo de interfaz que prepara el dato cifrado y la clave derivada.
3. Recuperar la dirección generada y extraer de ella el dato de validación destinado al reto.
4. Enviar ese dato exclusivamente al formulario oficial de Root-Me.

## Verificación

La solución fue reproducida contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se incluye en el repositorio.

## Notas adicionales

- Cifrar un dato en el navegador no lo protege si la clave y el descifrador se entregan al mismo cliente.
- La información sensible debe validarse y conservarse del lado servidor.
