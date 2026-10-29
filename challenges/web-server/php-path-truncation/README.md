# Web - Server — PHP - Path Truncation

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — PHP - Path Truncation](https://www.root-me.org/en/Challenges/Web-Server/PHP-Path-Truncation)

La aplicación añade una extensión segura a una ruta controlada por el usuario. En versiones afectadas, un nombre de ruta que alcanza el límite de longitud se trunca antes del sufijo añadido.

## Solución

1. Identificar el parámetro que compone una inclusión o lectura con un sufijo fijo.
2. Construir una ruta al recurso objetivo y añadir segmentos neutrales como `/./` hasta aproximarse al límite histórico de longitud de ruta de PHP.
3. Hacer que el sufijo aplicado por la aplicación quede más allá del límite y sea truncado, manteniendo la ruta al archivo objetivo.
4. Usar el resultado exclusivamente para validar en Root-Me.

## Estado de revalidación

El vector de truncamiento y el reto fueron identificados desde documentación pública. Falta confirmar el límite y el parámetro contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- No concatenar extensiones o rutas con datos de la petición; usar identificadores de recursos permitidos.
- Mantener el runtime actualizado: este comportamiento depende de versiones antiguas y límites específicos.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Path-Truncation)
- [PHP — Filesystem Security](https://www.php.net/manual/en/security.filesystem.php)
