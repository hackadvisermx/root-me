# Progreso — Root-Me

Inventario de la interfaz en inglés de Root-Me, consultado el **2026-10-28**. Se diferencia el avance de la cuenta en plataforma de los writeups que ya fueron reproducidos y publicados en este repositorio.

| Categoría | Catálogo | Validados en plataforma | Revalidados y documentados | Estado |
|---|---:|---:|---:|---|
| App - Script | 33 | 1 | 0 | ⏳ Pendiente de documentación retroactiva |
| App - System | 43 | 0 | 0 | ⏳ Sin validaciones previas |
| Cracking | 70 | 4 | 0 | ⏳ Pendiente de documentación retroactiva |
| Cryptanalysis | 75 | 4 | 0 | ⏳ Pendiente de documentación retroactiva |
| Forensic | 48 | 0 | 0 | ⏳ Sin validaciones previas |
| Network | 35 | 4 | 0 | ⏳ Pendiente de documentación retroactiva |
| Programming | 29 | 0 | 0 | ⏳ Sin validaciones previas |
| Realist | 62 | 0 | 0 | ⏳ Sin validaciones previas |
| Steganography | 24 | 0 | 0 | ⏳ Sin validaciones previas |
| Web - Client | 42 | 9 | 0 | ⏳ Pendiente de documentación retroactiva |
| Web - Server | 97 | 21 | 20 | 🚧 En documentación retroactiva |
| **Total** | **558** | **43** | **20** | **🚧 En curso** |

## Bitácora de revalidación

| Fecha | Reto | Resultado | Writeup |
|---|---|---|---|
| 2026-10-28 | HTML - Source code | Reproducido en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 5 puntos. | [web-server/html-source-code](challenges/web-server/html-source-code/README.md) |
| 2026-10-28 | HTTP - Open redirect | Reproducido en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 10 puntos. | [web-server/http-open-redirect](challenges/web-server/http-open-redirect/README.md) |
| 2026-10-28 | HTTP - User-agent | Reproducido con la cabecera `User-Agent` controlada; Root-Me confirma que la cuenta ya obtuvo los 10 puntos. | [web-server/http-user-agent](challenges/web-server/http-user-agent/README.md) |
| 2026-10-28 | Weak password | Reproducido con autenticación HTTP Basic en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 10 puntos. | [web-server/weak-password](challenges/web-server/weak-password/README.md) |
| 2026-10-28 | PHP - Command injection | Reproducido mediante inyección de comandos en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 10 puntos. | [web-server/php-command-injection](challenges/web-server/php-command-injection/README.md) |
| 2026-10-28 | Backup file | Reproducido al recuperar una copia de seguridad expuesta y autenticar en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 10 puntos. | [web-server/backup-file](challenges/web-server/backup-file/README.md) |
| 2026-10-28 | HTTP - Directory indexing | Reproducido al recorrer índices de directorio expuestos en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/http-directory-indexing](challenges/web-server/http-directory-indexing/README.md) |
| 2026-10-28 | HTTP - Headers | Reproducido al modificar la cabecera de petición indicada por la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/http-headers](challenges/web-server/http-headers/README.md) |
| 2026-10-28 | HTTP POST | Reproducido al modificar un parámetro de formulario que la instancia oficial confía al cliente; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/http-post](challenges/web-server/http-post/README.md) |
| 2026-10-28 | HTTP - Improper redirect | Reproducido al conservar el cuerpo de una redirección de la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/http-improper-redirect](challenges/web-server/http-improper-redirect/README.md) |
| 2026-10-28 | HTTP - Verb tampering | Reproducido con un método HTTP alternativo en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/http-verb-tampering](challenges/web-server/http-verb-tampering/README.md) |
| 2026-10-28 | Install files | Reproducido al acceder al instalador expuesto en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 15 puntos. | [web-server/install-files](challenges/web-server/install-files/README.md) |
| 2026-10-28 | CRLF | Reproducido al inyectar un salto de línea en el registro de autenticación de la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 20 puntos. | [web-server/crlf](challenges/web-server/crlf/README.md) |
| 2026-10-28 | File upload - Double extensions | Reproducido al subir y ejecutar un archivo de prueba con doble extensión en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 20 puntos. | [web-server/file-upload-double-extensions](challenges/web-server/file-upload-double-extensions/README.md) |
| 2026-10-28 | File upload - MIME type | Reproducido al falsear el tipo MIME de una carga en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 20 puntos. | [web-server/file-upload-mime-type](challenges/web-server/file-upload-mime-type/README.md) |
| 2026-10-28 | HTTP - Cookies | Reproducido al manipular la cookie de rol de la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 20 puntos. | [web-server/http-cookies](challenges/web-server/http-cookies/README.md) |
| 2026-10-28 | Directory traversal | Reproducido al acceder a un directorio no previsto mediante el parámetro de galería de la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 25 puntos. | [web-server/directory-traversal](challenges/web-server/directory-traversal/README.md) |
| 2026-10-28 | File upload - Null byte | Reproducido al cargar un archivo con byte nulo codificado en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 25 puntos. | [web-server/file-upload-null-byte](challenges/web-server/file-upload-null-byte/README.md) |
| 2026-10-28 | PHP - assert() | Reproducido mediante evaluación insegura en `assert()` en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 25 puntos. | [web-server/php-assert](challenges/web-server/php-assert/README.md) |
| 2026-10-28 | PHP - Filters | Reproducido mediante el wrapper `php://filter` en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 25 puntos. | [web-server/php-filters](challenges/web-server/php-filters/README.md) |

## Criterio de registro

- Un writeup cuenta como documentado cuando explica el reto de forma reproducible y no incluye flags ni credenciales.
- Las cantidades del catálogo y las validaciones de la cuenta se obtienen desde [Root-Me Challenges](https://www.root-me.org/en/Challenges/) en inglés, que es la fuente de verdad de este seguimiento.
- Los retos que ya aparezcan resueltos en la cuenta se registrarán por separado de los writeups pendientes, para no confundir progreso en plataforma con documentación local.
