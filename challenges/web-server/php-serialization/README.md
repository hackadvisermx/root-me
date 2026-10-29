# Web - Server — PHP - Serialization

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — PHP - Serialization](https://www.root-me.org/en/Challenges/Web-Server/PHP-Serialization)

La cookie `autologin` se pasa a `unserialize()` y la autenticación compara la contraseña con `==`. Un valor booleano verdadero satisface la comparación débil contra una contraseña de cadena no vacía.

## Solución

1. Iniciar sesión como invitado y observar la estructura serializada de `autologin`.
2. Construir un arreglo serializado con el usuario administrativo y un booleano para la contraseña:

   ```text
   a:2:{s:5:"login";s:10:"superadmin";s:8:"password";b:1;}
   ```

3. Codificar el valor para transporte HTTP y sustituir únicamente la cookie `autologin` en la instancia autorizada.
4. La comparación laxa trata el booleano como equivalente a la contraseña no vacía; usar el resultado exclusivamente para Root-Me.

## Estado de revalidación

El código de autenticación y el vector fueron contrastados con un writeup público. Falta reproducirlo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Nunca aplicar `unserialize()` a datos controlados por clientes; usar formatos de datos seguros y sesiones del lado servidor.
- Las comprobaciones de credenciales deben usar comparaciones estrictas y funciones de verificación de contraseñas.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Serialization)
- [PHP — serialize](https://www.php.net/manual/en/function.serialize.php)
