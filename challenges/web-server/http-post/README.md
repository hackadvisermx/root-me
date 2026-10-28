# Web - Server — HTTP POST

## Descripción

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 15
- **Reto:** [Root-Me — HTTP POST](https://www.root-me.org/en/Challenges/Web-Server/HTTP-POST)

La aplicación muestra un marcador generado por el servidor. Al observar la petición del formulario se aprecia que el valor del marcador se reenvía desde el cliente y el servidor confía en él para decidir el resultado.

## Solución

1. Enviar el formulario una vez y revisar el cuerpo `application/x-www-form-urlencoded` de la petición.
2. Repetir la petición sustituyendo el marcador por un entero alto, sin alterar parámetros ajenos al reto:

   ```bash
   curl -X POST \\
     -d 'score=100000000&generate=Give+a+try%21' \\
     http://challenge01.root-me.org/web-serveur/ch56/
   ```

3. La instancia acepta el marcador controlado por el cliente y muestra el dato de validación.
4. Registrar ese dato únicamente en Root-Me.

La cuenta ya tenía el reto validado. La petición manipulada volvió a producir la respuesta de validación antes de documentarlo.

## Notas adicionales

- Un valor que determina autorización, premios o progreso no debe ser una afirmación sin verificar enviada por el cliente.
- El servidor debe conservar el estado relevante o recalcularlo desde datos confiables del lado servidor.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-POST)
- [OWASP — Parameter Tampering](https://owasp.org/www-community/attacks/Web_Parameter_Tampering)
