# Web - Server — SQL Truncation

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — SQL Truncation](https://www.root-me.org/en/Challenges/Web-Server/SQL-Truncation)

El registro acepta un nombre de usuario más largo que la columna `VARCHAR(12)`. Al truncarse silenciosamente, una cuenta nueva puede quedar con el mismo nombre lógico que el administrador.

## Solución

1. Revisar el comentario de esquema expuesto en el registro e identificar el límite de `login`.
2. Registrar una cuenta que empiece con `admin`, complete el límite con espacios y añada caracteres después del límite.
3. Elegir una contraseña propia para esa cuenta; el almacenamiento trunca el login a la identidad administrativa.
4. Acceder al área administrativa con la contraseña creada y usar el resultado exclusivamente en Root-Me.

## Estado de revalidación

La longitud de columna, el truncamiento y el flujo de autenticación se contrastaron con documentación del reto. Falta reproducirlo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Rechazar entradas que excedan el límite antes de persistir; nunca truncarlas silenciosamente en credenciales.
- Aplicar restricciones de unicidad y comparaciones canónicas consistentes en registro e inicio de sesión.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-Truncation)
- [OWASP — Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
