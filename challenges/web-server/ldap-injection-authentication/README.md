# Web - Server — LDAP injection - Authentication

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — LDAP injection - Authentication](https://www.root-me.org/en/Challenges/Web-Server/LDAP-injection-authentication)

Los valores de usuario y contraseña se interpolan directamente en un filtro LDAP. El cierre del filtro y el uso de comodines permiten crear una condición alternativa que coincide con una entrada válida.

## Solución

1. Confirmar la concatenación directa con un carácter de cierre que produzca un error de sintaxis controlado.
2. Enviar los parámetros de formulario:

   ```text
   username=*)(|(userPassword=
   password=*)
   ```

3. El filtro construido desde una forma como `(&(uid=<username>)(userPassword=<password>))` incorpora un `OR` y el comodín LDAP, obteniendo una coincidencia válida.
4. Usar los atributos de la entrada devuelta únicamente para validar en Root-Me.

## Estado de revalidación

El filtro resultante y el vector fueron contrastados con documentación pública. Falta ejecutarlo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las consultas LDAP deben usar APIs parametrizadas o un escape contextual completo de valores.
- El servicio de directorio debe devolver solo atributos mínimos y no usar mensajes de error que revelen filtros internos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/LDAP-injection-authentication)
- [OWASP — LDAP Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/LDAP_Injection_Prevention_Cheat_Sheet.html)
