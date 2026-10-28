# Web - Server — HTTP - Open redirect

## Descripción

> **Enunciado oficial:** “Find a way to make a redirection to a domain other than those showed on the web page.”

- **Categoría:** Web - Server
- **Dificultad:** Very easy
- **Puntos:** 10
- **Autor:** Swissky
- **Reto:** [Root-Me — HTTP - Open redirect](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Open-redirect)

La instancia muestra enlaces a redes sociales. Cada enlace usa los parámetros `url` y `h`; el reto consiste en construir un enlace válido que redirija a un dominio distinto de los tres predefinidos.

## Solución

1. Inspeccionar los tres enlaces iniciales. Un ejemplo tiene la forma:

   ```text
   ?url=https://facebook.com&h=<hash>
   ```

2. Calcular el MD5 de la URL original y comprobar que coincide con `h`.
3. Elegir un dominio de prueba distinto, calcular su MD5 y construir la misma pareja de parámetros.

   ```bash
   destination='https://example.org'
   hash=$(printf '%s' "$destination" | md5)                    # macOS
   # En GNU/Linux: hash=$(printf '%s' "$destination" | md5sum | cut -d' ' -f1)
   ```

4. Abrir la URL resultante. La aplicación acepta el hash, muestra brevemente la respuesta de validación y ejecuta la redirección mediante JavaScript.
5. Para ver la respuesta antes de que el navegador navegue, abrir el código fuente de la URL resultante o desactivar JavaScript temporalmente en un contexto aislado.
6. Enviar la respuesta obtenida al formulario de validación de Root-Me.

Root-Me confirmó que la cuenta ya había obtenido los 10 puntos después de repetir el proceso.

## Notas adicionales

- `h` no aporta integridad ni control de acceso: se calcula a partir de un valor controlado por el usuario y no incluye ningún secreto.
- El fallo es un **open redirect**: una aplicación de confianza puede enviar al usuario a un destino arbitrario, una técnica común en campañas de phishing.
- Una mitigación correcta es usar una lista de destinos permitidos del lado servidor o guardar identificadores internos de redirección en lugar de aceptar URLs completas del cliente.
- La respuesta de validación no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Open-redirect)
- [CWE-601: URL Redirection to Untrusted Site](https://cwe.mitre.org/data/definitions/601.html)
