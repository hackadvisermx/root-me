# Web - Server — XSLT - Code execution

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — XSLT - Code execution](https://www.root-me.org/en/Challenges/Web-Server/XSLT-Code-execution)

El parámetro `xsl` carga una hoja XSL remota controlada por el usuario. El procesador expone el namespace PHP de XSLT, por lo que una transformación remota puede llamar funciones PHP en el contexto de la instancia.

## Solución

1. Hospedar una hoja `probe.xsl` propia y pasar su URL codificada mediante `?xsl=`.
2. Confirmar la transformación con un dato no sensible como `system-property('xsl:vendor')`.
3. Usar la extensión `http://php.net/xsl` y `php:function(...)` para enumerar el directorio de trabajo.
4. Tras identificar el subdirectorio objetivo, leer únicamente el recurso de validación del reto y usar el resultado en Root-Me.

## Estado de revalidación

La carga de hoja remota y la exposición de funciones PHP fueron comprobadas en documentación pública. Falta reproducir el flujo contra la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Las hojas XSL no deben provenir de URL controladas por el usuario.
- Deshabilitar extensiones PHP y el acceso a archivos/red no imprescindibles en el procesador XSLT.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XSLT-Code-execution)
- [PHP — XSLTProcessor](https://www.php.net/manual/en/class.xsltprocessor.php)
