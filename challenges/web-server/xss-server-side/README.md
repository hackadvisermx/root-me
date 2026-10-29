# Web - Server — XSS - Server Side

## Descripción

- **Puntos:** 20
- **Reto:** [Root-Me — XSS - Server Side](https://www.root-me.org/en/Challenges/Web-Server/XSS-Server-Side)

La aplicación crea certificados PDF desde datos de perfil. Aunque el texto libre se escapa, un campo persistente del perfil se inserta como HTML durante la generación y el motor de PDF interpreta recursos locales.

## Solución

1. Crear una cuenta efímera en la instancia Start.
2. Colocar una inclusión HTML local en un campo de nombre que se muestre en el certificado:

   ```html
   <iframe src="file:///flag.txt"></iframe>
   ```

3. Iniciar sesión con esa cuenta y generar el PDF.
4. El generador interpreta el `iframe` en su contexto de servidor e incorpora el contenido local en el documento.
5. Usar el resultado únicamente para validarlo en Root-Me.

## Estado de revalidación

La técnica se documentó a partir del enunciado y un análisis público del reto. Falta iniciar la instancia autenticada, reproducir el flujo completo, validar y registrar el «Like»; hasta entonces no se cuenta como validado.

## Notas adicionales

- Escapar datos en una vista no basta si esos mismos datos llegan después a un motor HTML/PDF con un contexto distinto.
- El generador de documentos debe ejecutarse con privilegios mínimos, sin acceso a archivos sensibles y sin permitir esquemas `file:` no necesarios.
- La cuenta usada para la prueba debe ser efímera y la respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XSS-Server-Side)
- [Análisis técnico del reto](https://internet-lab.ru/ctf_xss_server_side)
