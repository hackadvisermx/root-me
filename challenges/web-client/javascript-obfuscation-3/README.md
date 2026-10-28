# Web - Client — Javascript - Obfuscation 3

## Descripción

- **Dificultad:** Hard
- **Puntos:** 30
- **Reto:** [Root-Me — Javascript - Obfuscation 3](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-3)

La página transforma una cadena con escapes en una lista de números decimales. El prompt visible es un señuelo: la solución está en reconstruir la cadena que el navegador ya recibió.

## Solución

1. Extraer la cadena de escapes `\x` del script y decodificarla a texto.
2. Separar la lista decimal resultante y convertir cada número a carácter:

   ```js
   decimal.split(',').map(Number).map(String.fromCharCode).join('');
   ```

3. Usar el resultado exclusivamente en el formulario de validación de Root-Me.

## Estado de revalidación

La cuenta ya tenía el reto validado y su «Like» se registró. La instancia histórica entrega actualmente una página sin el JavaScript del reto; la técnica fue reconstruida sin incluir la respuesta.

## Notas adicionales

- Un prompt o interfaz bloqueante no protege el contenido que el navegador ya descargó.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-3)
- [MDN — String.fromCharCode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
