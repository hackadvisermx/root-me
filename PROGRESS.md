# Progreso — Root-Me

Inventario de la interfaz en inglés de Root-Me, consultado el **2026-10-28**. Se diferencia el avance de la cuenta en plataforma de los writeups que ya fueron reproducidos y publicados en este repositorio.

| Categoría | Catálogo | Validados en plataforma | Revalidados y documentados | Estado |
|---|---:|---:|---:|---|
| App - Script | 33 | 1 | 1 | ✅ Documentación retroactiva completa |
| App - System | 43 | 0 | 0 | ⏳ Sin validaciones previas |
| Cracking | 70 | 4 | 4 | ✅ Documentación retroactiva completa |
| Cryptanalysis | 75 | 4 | 4 | ✅ Documentación retroactiva completa |
| Forensic | 48 | 0 | 0 | ⏳ Sin validaciones previas |
| Network | 35 | 4 | 4 | ✅ Documentación retroactiva completa |
| Programming | 29 | 0 | 0 | ⏳ Sin validaciones previas |
| Realist | 62 | 0 | 0 | ⏳ Sin validaciones previas |
| Steganography | 24 | 0 | 0 | ⏳ Sin validaciones previas |
| Web - Client | 42 | 9 | 9 | ✅ Documentación retroactiva completa |
| Web - Server | 97 | 27 | 27 | 🚧 Ampliación en orden de catálogo |
| **Total** | **558** | **49** | **49** | **🚧 Ampliación en curso** |

## Web - Server — orden activo de resolución

La ampliación comenzó con el primer reto marcado con X en el catálogo de Web Server. La numeración sigue el orden visual actual de ese catálogo; cada fila se actualizará antes de iniciar la siguiente.

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | HTTP - IP restriction bypass | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/http-ip-restriction-bypass/README.md) |
| 2 | API - Broken Access | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/api-broken-access/README.md) |
| 3 | Nginx - Alias Misconfiguration | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/nginx-alias-misconfiguration/README.md) |
| 4 | Nginx - Root Location Misconfiguration | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/nginx-root-location-misconfiguration/README.md) |
| 5 | API - Mass Assignment | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/api-mass-assignment/README.md) |
| 6 | Flask - Unsecure session | ✅ Validado; palomita y «Like» confirmados | [writeup](challenges/web-server/flask-unsecure-session/README.md) |
| 7 | GraphQL - Introspection | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/graphql-introspection/README.md) |
| 8 | Insecure Code Management | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/insecure-code-management/README.md) |
| 9 | JWT - Introduction | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-introduction/README.md) |
| 10 | XSS - Server Side | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xss-server-side/README.md) |
| 11 | JWT - Revoked token | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-revoked-token/README.md) |
| 12 | JWT - Weak secret | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-weak-secret/README.md) |
| 13 | JWT - Unsecure File Signature | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-unsecure-file-signature/README.md) |
| 14 | PHP - Apache configuration | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-apache-configuration/README.md) |
| 15 | PHP - preg_replace() | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-preg-replace/README.md) |
| 16 | PHP - type juggling | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-type-juggling/README.md) |
| 17 | Remote File Inclusion | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/remote-file-inclusion/README.md) |
| 18 | Ruby on Rails - ransack | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/ruby-on-rails-ransack/README.md) |
| 19 | SQL injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-authentication/README.md) |
| 20 | SQL injection - Authentication - GBK | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-authentication-gbk/README.md) |
| 21 | SQL injection - String | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-string/README.md) |
| 22 | XSLT - Code execution | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/xslt-code-execution/README.md) |
| 23 | Elixir - EEx | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/elixir-eex/README.md) |
| 24 | JWT - Unsecure Key Handling | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-unsecure-key-handling/README.md) |
| 25 | LDAP injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/ldap-injection-authentication/README.md) |
| 26 | Node - Serialize | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/node-serialize/README.md) |
| 27 | NoSQL injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/nosql-injection-authentication/README.md) |
| 28 | PHP - Path Truncation | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/php-path-truncation/README.md) |
| 29 | PHP - Serialization | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-serialization/README.md) |
| 30 | SQL injection - Numeric | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-numeric/README.md) |
| 31 | SQL Injection - Routed | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-routed/README.md) |
| 32 | SQL Truncation | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-truncation/README.md) |
| 33 | XML External Entity | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xml-external-entity/README.md) |
| 34 | XPath injection - Authentication | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xpath-injection-authentication/README.md) |
| 35 | Yaml - Deserialization | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/yaml-deserialization/README.md) |
| 36 | API - Broken Access 2 | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/api-broken-access-2/README.md) |
| 37 | GraphQL - Backend injection | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/graphql-backend-injection/README.md) |
| 38 | GraphQL - Mutation | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/graphql-mutation/README.md) |
| 39 | Java - Spring Boot | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/java-spring-boot/README.md) |
| 40 | Local File Inclusion - Wrappers | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/local-file-inclusion-wrappers/README.md) |
| 41 | PHP - Eval | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-eval/README.md) |
| 42 | PHP - Eval - Advanced filters bypass | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-eval-advanced-filters-bypass/README.md) |
| 43 | SQL injection - Error | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-error/README.md) |
| 44 | SQL injection - Insert | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-insert/README.md) |
| 45 | SQL injection - File reading | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-file-reading/README.md) |
| 46 | XPath injection - String | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/xpath-injection-string/README.md) |
| 47 | File upload - Polyglot | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/file-upload-polyglot/README.md) |
| 48 | NodeJS - Prototype Pollution Bypass | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/nodejs-prototype-pollution-bypass/README.md) |
| 49 | NoSQL injection - blind | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/nosql-injection-blind/README.md) |
| 50 | SQL injection - Time based | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-time-based/README.md) |

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
| 2026-10-28 | PHP - register globals | Reproducido al inicializar indebidamente el estado de sesión desde la query de la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 25 puntos. | [web-server/php-register-globals](challenges/web-server/php-register-globals/README.md) |
| 2026-10-28 | HTML - disabled buttons | Reproducido al habilitar controles HTML únicamente en la instancia oficial; Root-Me confirma que la cuenta ya obtuvo los 5 puntos. | [web-client/html-disabled-buttons](challenges/web-client/html-disabled-buttons/README.md) |
| 2026-10-28 | Javascript - Authentication | Reconstrucción retroactiva de la autenticación cliente; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-authentication](challenges/web-client/javascript-authentication/README.md) |
| 2026-10-28 | Javascript - Source | Reconstrucción retroactiva mediante recursos JavaScript; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-source](challenges/web-client/javascript-source/README.md) |
| 2026-10-28 | Javascript - Authentication 2 | Reconstrucción retroactiva de la comprobación cliente; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-authentication-2](challenges/web-client/javascript-authentication-2/README.md) |
| 2026-10-28 | Javascript - Obfuscation 1 | Reconstrucción retroactiva de la decodificación cliente; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-obfuscation-1](challenges/web-client/javascript-obfuscation-1/README.md) |
| 2026-10-28 | Javascript - Obfuscation 2 | Reconstrucción retroactiva de la ofuscación cliente; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-obfuscation-2](challenges/web-client/javascript-obfuscation-2/README.md) |
| 2026-10-28 | Javascript - Native code | Reconstrucción retroactiva con depuración de JavaScript; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-native-code](challenges/web-client/javascript-native-code/README.md) |
| 2026-10-28 | Javascript - Obfuscation 3 | Reconstrucción retroactiva de conversiones de cadenas; la cuenta confirma la resolución y se registró «Like». | [web-client/javascript-obfuscation-3](challenges/web-client/javascript-obfuscation-3/README.md) |
| 2026-10-28 | XSS - Stored 1 | Reconstrucción retroactiva del flujo XSS almacenado; la cuenta confirma la resolución y se registró «Like». | [web-client/xss-stored-1](challenges/web-client/xss-stored-1/README.md) |
| 2026-10-28 | FTP - authentication | Reproducido al analizar comandos FTP en texto claro de la captura oficial; se registró «Like». | [network/ftp-authentication](challenges/network/ftp-authentication/README.md) |
| 2026-10-28 | TELNET - authentication | Reproducido al reconstruir la autenticación desde la captura Telnet oficial; se registró «Like». | [network/telnet-authentication](challenges/network/telnet-authentication/README.md) |
| 2026-10-28 | ETHERNET - frame | Reproducido al decodificar la autorización HTTP Basic del volcado oficial; se registró «Like». | [network/ethernet-frame](challenges/network/ethernet-frame/README.md) |
| 2026-10-28 | Twitter authentication | Reproducido al analizar una cabecera de autorización HTTP en la captura oficial; se registró «Like». | [network/twitter-authentication](challenges/network/twitter-authentication/README.md) |
| 2026-10-28 | ELF x86 - 0 protection | Recurso oficial revisado mediante análisis estático; la cuenta confirma la resolución y se registró «Like». | [cracking/elf-x86-0-protection](challenges/cracking/elf-x86-0-protection/README.md) |
| 2026-10-28 | ELF x86 - Basic | Recurso oficial revisado mediante análisis de comparaciones x86; la cuenta confirma la resolución y se registró «Like». | [cracking/elf-x86-basic](challenges/cracking/elf-x86-basic/README.md) |
| 2026-10-28 | PE x86 - 0 protection | Recurso oficial revisado mediante análisis estático de PE; la cuenta confirma la resolución y se registró «Like». | [cracking/pe-x86-0-protection](challenges/cracking/pe-x86-0-protection/README.md) |
| 2026-10-28 | ELF C++ - 0 protection | Recurso oficial revisado mediante análisis de la rutina C++; la cuenta confirma la resolución y se registró «Like». | [cracking/elf-cpp-0-protection](challenges/cracking/elf-cpp-0-protection/README.md) |
| 2026-10-28 | Encoding - ASCII | Técnica de conversión ASCII documentada; la cuenta confirma la resolución y se registró «Like». | [cryptanalysis/encoding-ascii](challenges/cryptanalysis/encoding-ascii/README.md) |
| 2026-10-28 | Encoding - UU | Técnica de decodificación uuencode documentada; la cuenta confirma la resolución y se registró «Like». | [cryptanalysis/encoding-uu](challenges/cryptanalysis/encoding-uu/README.md) |
| 2026-10-28 | Hash - Message Digest 5 | Técnica de comparación MD5 documentada; la cuenta confirma la resolución y se registró «Like». | [cryptanalysis/hash-md5](challenges/cryptanalysis/hash-md5/README.md) |
| 2026-10-28 | Hash - SHA-2 | Técnica de comparación SHA-2 documentada; la cuenta confirma la resolución y se registró «Like». | [cryptanalysis/hash-sha-2](challenges/cryptanalysis/hash-sha-2/README.md) |
| 2026-10-28 | Bash - System 1 | Técnica de PATH hijacking en binario SUID documentada; la cuenta confirma la resolución y se registró «Like». | [app-script/bash-system-1](challenges/app-script/bash-system-1/README.md) |
| 2026-10-28 | HTTP - IP restriction bypass | Resuelto y validado al declarar una IP privada en `X-Forwarded-For`; la palomita y el «Like» fueron confirmados. | [web-server/http-ip-restriction-bypass](challenges/web-server/http-ip-restriction-bypass/README.md) |
| 2026-10-28 | API - Broken Access | Resuelto y validado al consultar sin autorización el objeto administrativo con ID predecible; la palomita y el «Like» fueron confirmados. | [web-server/api-broken-access](challenges/web-server/api-broken-access/README.md) |
| 2026-10-28 | Nginx - Alias Misconfiguration | Resuelto y validado mediante el patrón `assets../` de alias traversal; la palomita y el «Like» fueron confirmados. | [web-server/nginx-alias-misconfiguration](challenges/web-server/nginx-alias-misconfiguration/README.md) |
| 2026-10-28 | Nginx - Root Location Misconfiguration | Resuelto y validado al leer configuración Nginx expuesta por el `root` global; la palomita y el «Like» fueron confirmados. | [web-server/nginx-root-location-misconfiguration](challenges/web-server/nginx-root-location-misconfiguration/README.md) |
| 2026-10-28 | API - Mass Assignment | Resuelto y validado al elevar el rol con una propiedad no permitida por el flujo normal; la palomita y el «Like» fueron confirmados. | [web-server/api-mass-assignment](challenges/web-server/api-mass-assignment/README.md) |
| 2026-10-28 | Flask - Unsecure session | Resuelto y validado al forjar una sesión Flask administrativa firmada con clave débil; la palomita y el «Like» fueron confirmados. | [web-server/flask-unsecure-session](challenges/web-server/flask-unsecure-session/README.md) |

## Criterio de registro

- Un writeup cuenta como documentado cuando explica el reto de forma reproducible y no incluye flags ni credenciales. Desde el reto 44, las validaciones nuevas se resuelven en el orden del catálogo y se registran también en Root-Me.
- Las cantidades del catálogo y las validaciones de la cuenta se obtienen desde [Root-Me Challenges](https://www.root-me.org/en/Challenges/) en inglés, que es la fuente de verdad de este seguimiento.
- Los retos que ya aparezcan resueltos en la cuenta se registrarán por separado de los writeups pendientes, para no confundir progreso en plataforma con documentación local.
