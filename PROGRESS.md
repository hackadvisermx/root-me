# Progreso — Root-Me

Inventario de la interfaz en inglés de Root-Me, consultado el **2026-10-28**. Se diferencia el avance de la cuenta en plataforma de los writeups que ya fueron reproducidos y publicados en este repositorio.

| Categoría | Catálogo | Validados en plataforma | Validados y documentados | Estado |
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
| Web - Server | 97 | 28 | 28 | 🚧 Ampliación en orden de catálogo |
| **Total** | **558** | **50** | **50** | **🚧 Ampliación en curso** |

## Desglose de validados y documentados

Los números de esta sección son el detalle trazable del concentrado superior. Cada categoría se presenta en el mismo orden en que Root-Me muestra su catálogo.

| Categoría | Validados y documentados | Desglose |
|---|---:|---|
| App - Script | 1 | [Bash - System 1](challenges/app-script/bash-system-1/README.md) |
| Cracking | 4 | [ELF x86 - 0 protection](challenges/cracking/elf-x86-0-protection/README.md), [ELF x86 - Basic](challenges/cracking/elf-x86-basic/README.md), [PE x86 - 0 protection](challenges/cracking/pe-x86-0-protection/README.md), [ELF C++ - 0 protection](challenges/cracking/elf-cpp-0-protection/README.md) |
| Cryptanalysis | 4 | [Encoding - ASCII](challenges/cryptanalysis/encoding-ascii/README.md), [Encoding - UU](challenges/cryptanalysis/encoding-uu/README.md), [Hash - MD5](challenges/cryptanalysis/hash-md5/README.md), [Hash - SHA-2](challenges/cryptanalysis/hash-sha-2/README.md) |
| Network | 4 | [FTP - authentication](challenges/network/ftp-authentication/README.md), [TELNET - authentication](challenges/network/telnet-authentication/README.md), [ETHERNET - frame](challenges/network/ethernet-frame/README.md), [Twitter authentication](challenges/network/twitter-authentication/README.md) |
| Web - Client | 9 | [HTML - disabled buttons](challenges/web-client/html-disabled-buttons/README.md), [Javascript - Authentication](challenges/web-client/javascript-authentication/README.md), [Javascript - Source](challenges/web-client/javascript-source/README.md), [Javascript - Authentication 2](challenges/web-client/javascript-authentication-2/README.md), [Javascript - Obfuscation 1](challenges/web-client/javascript-obfuscation-1/README.md), [Javascript - Obfuscation 2](challenges/web-client/javascript-obfuscation-2/README.md), [Javascript - Native code](challenges/web-client/javascript-native-code/README.md), [Javascript - Obfuscation 3](challenges/web-client/javascript-obfuscation-3/README.md), [XSS - Stored 1](challenges/web-client/xss-stored-1/README.md) |
| Web - Server | 28 | **7** del [orden activo](#web---server--orden-activo-de-resolución) + **21** [históricos](#web---server--validaciones-históricas-ya-documentadas) |
| **Total** | **50** | **1 + 4 + 4 + 4 + 9 + 28** |

## Web - Server — catálogo y resolución en orden de aparición

Esta es la única secuencia de Web Server y reproduce el orden visual actual del catálogo oficial. Incluye los **28** retos validados y documentados, los writeups pendientes de validación y los retos todavía sin documentar.

| # catálogo | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | HTML - Source code | ✅ Validado y documentado | [writeup](challenges/web-server/html-source-code/README.md) |
| 2 | HTTP - IP restriction bypass | ✅ Validado y documentado | [writeup](challenges/web-server/http-ip-restriction-bypass/README.md) |
| 3 | HTTP - Open redirect | ✅ Validado y documentado | [writeup](challenges/web-server/http-open-redirect/README.md) |
| 4 | HTTP - User-agent | ✅ Validado y documentado | [writeup](challenges/web-server/http-user-agent/README.md) |
| 5 | Weak password | ✅ Validado y documentado | [writeup](challenges/web-server/weak-password/README.md) |
| 6 | PHP - Command injection | ✅ Validado y documentado | [writeup](challenges/web-server/php-command-injection/README.md) |
| 7 | API - Broken Access | ✅ Validado y documentado | [writeup](challenges/web-server/api-broken-access/README.md) |
| 8 | Backup file | ✅ Validado y documentado | [writeup](challenges/web-server/backup-file/README.md) |
| 9 | HTTP - Directory indexing | ✅ Validado y documentado | [writeup](challenges/web-server/http-directory-indexing/README.md) |
| 10 | HTTP - Headers | ✅ Validado y documentado | [writeup](challenges/web-server/http-headers/README.md) |
| 11 | HTTP - POST | ✅ Validado y documentado | [writeup](challenges/web-server/http-post/README.md) |
| 12 | HTTP - Improper redirect | ✅ Validado y documentado | [writeup](challenges/web-server/http-improper-redirect/README.md) |
| 13 | HTTP - Verb tampering | ✅ Validado y documentado | [writeup](challenges/web-server/http-verb-tampering/README.md) |
| 14 | Install files | ✅ Validado y documentado | [writeup](challenges/web-server/install-files/README.md) |
| 15 | Nginx - Alias Misconfiguration | ✅ Validado y documentado | [writeup](challenges/web-server/nginx-alias-misconfiguration/README.md) |
| 16 | Nginx - Root Location Misconfiguration | ✅ Validado y documentado | [writeup](challenges/web-server/nginx-root-location-misconfiguration/README.md) |
| 17 | API - Mass Assignment | ✅ Validado y documentado | [writeup](challenges/web-server/api-mass-assignment/README.md) |
| 18 | CRLF | ✅ Validado y documentado | [writeup](challenges/web-server/crlf/README.md) |
| 19 | File upload - Double extensions | ✅ Validado y documentado | [writeup](challenges/web-server/file-upload-double-extensions/README.md) |
| 20 | File upload - MIME type | ✅ Validado y documentado | [writeup](challenges/web-server/file-upload-mime-type/README.md) |
| 21 | Flask - Unsecure session | ✅ Validado y documentado | [writeup](challenges/web-server/flask-unsecure-session/README.md) |
| 22 | GraphQL - Introspection | ✅ Validado y documentado | [writeup](challenges/web-server/graphql-introspection/README.md) |
| 23 | HTTP - Cookies | ✅ Validado y documentado | [writeup](challenges/web-server/http-cookies/README.md) |
| 24 | Insecure Code Management | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/insecure-code-management/README.md) |
| 25 | JWT - Introduction | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-introduction/README.md) |
| 26 | XSS - Server Side | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xss-server-side/README.md) |
| 27 | Directory traversal | ✅ Validado y documentado | [writeup](challenges/web-server/directory-traversal/README.md) |
| 28 | File upload - Null byte | ✅ Validado y documentado | [writeup](challenges/web-server/file-upload-null-byte/README.md) |
| 29 | JWT - Revoked token | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-revoked-token/README.md) |
| 30 | JWT - Weak secret | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-weak-secret/README.md) |
| 31 | JWT - Unsecure File Signature | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-unsecure-file-signature/README.md) |
| 32 | PHP - assert() | ✅ Validado y documentado | [writeup](challenges/web-server/php-assert/README.md) |
| 33 | PHP - Apache configuration | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-apache-configuration/README.md) |
| 34 | PHP - Filters | ✅ Validado y documentado | [writeup](challenges/web-server/php-filters/README.md) |
| 35 | PHP - register globals | ✅ Validado y documentado | [writeup](challenges/web-server/php-register-globals/README.md) |
| 36 | PHP - Remote Xdebug | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Remote-Xdebug) |
| 37 | Python - Server-side Template Injection Introduction | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Python-Server-side-Template-Injection-Introduction) |
| 38 | File upload - ZIP | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/File-upload-ZIP) |
| 39 | Flask - Development server | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Flask-Development-server) |
| 40 | GraphQL - Injection | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/GraphQL-Injection) |
| 41 | Command injection - Filter bypass | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Command-injection-Filter-bypass) |
| 42 | Java - Server-side Template Injection | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Java-Server-side-Template-Injection) |
| 43 | JWT - Public key | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Public-key) |
| 44 | JWT - Header Injection | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Header-Injection) |
| 45 | Local File Inclusion | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion) |
| 46 | Local File Inclusion - Double encoding | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Local-File-Inclusion-Double-encoding) |
| 47 | Nginx - SSRF Misconfiguration | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Nginx-SSRF-Misconfiguration) |
| 48 | Node - Eval | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Node-Eval) |
| 49 | PHP - Loose Comparison | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Loose-Comparison) |
| 50 | PHP - preg_replace() | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-preg-replace/README.md) |
| 51 | PHP - type juggling | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-type-juggling/README.md) |
| 52 | Remote File Inclusion | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/remote-file-inclusion/README.md) |
| 53 | Ruby on Rails - ransack | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/ruby-on-rails-ransack/README.md) |
| 54 | SQL injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-authentication/README.md) |
| 55 | SQL injection - Authentication - GBK | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-authentication-gbk/README.md) |
| 56 | SQL injection - String | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-string/README.md) |
| 57 | XSLT - Code execution | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/xslt-code-execution/README.md) |
| 58 | Elixir - EEx | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/elixir-eex/README.md) |
| 59 | JWT - Unsecure Key Handling | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/jwt-unsecure-key-handling/README.md) |
| 60 | LDAP injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/ldap-injection-authentication/README.md) |
| 61 | Node - Serialize | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/node-serialize/README.md) |
| 62 | NoSQL injection - Authentication | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/nosql-injection-authentication/README.md) |
| 63 | PHP - Path Truncation | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/php-path-truncation/README.md) |
| 64 | PHP - Serialization | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-serialization/README.md) |
| 65 | SQL injection - Numeric | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-numeric/README.md) |
| 66 | SQL Injection - Routed | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-routed/README.md) |
| 67 | SQL Truncation | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-truncation/README.md) |
| 68 | XML External Entity | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xml-external-entity/README.md) |
| 69 | XPath injection - Authentication | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/xpath-injection-authentication/README.md) |
| 70 | Yaml - Deserialization | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/yaml-deserialization/README.md) |
| 71 | API - Broken Access 2 | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/api-broken-access-2/README.md) |
| 72 | GraphQL - Backend injection | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/graphql-backend-injection/README.md) |
| 73 | GraphQL - Mutation | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/graphql-mutation/README.md) |
| 74 | Java - Spring Boot | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/java-spring-boot/README.md) |
| 75 | Local File Inclusion - Wrappers | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/local-file-inclusion-wrappers/README.md) |
| 76 | PHP - Eval | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-eval/README.md) |
| 77 | PHP - Eval - Advanced filters bypass | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/php-eval-advanced-filters-bypass/README.md) |
| 78 | SQL injection - Error | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-error/README.md) |
| 79 | SQL injection - Insert | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-insert/README.md) |
| 80 | SQL injection - File reading | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-file-reading/README.md) |
| 81 | XPath injection - String | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/xpath-injection-string/README.md) |
| 82 | File upload - Polyglot | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/file-upload-polyglot/README.md) |
| 83 | NodeJS - Prototype Pollution Bypass | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/nodejs-prototype-pollution-bypass/README.md) |
| 84 | NoSQL injection - Blind | 🟡 Técnica documentada; pendiente de validación y «Like» | [writeup](challenges/web-server/nosql-injection-blind/README.md) |
| 85 | SQL injection - Time based | 🟡 Técnica reproducida; pendiente de validación y «Like» | [writeup](challenges/web-server/sql-injection-time-based/README.md) |
| 86 | Java - Custom gadget deserialization | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Java-Custom-gadget-deserialization) |
| 87 | NodeJS - vm escape | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/NodeJS-vm-escape) |
| 88 | Server Side Request Forgery | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Server-Side-Request-Forgery) |
| 89 | SQL injection - Blind | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Blind) |
| 90 | LDAP injection - Blind | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/LDAP-injection-Blind) |
| 91 | PHP - Unserialize overflow | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Unserialize-overflow) |
| 92 | PHP - Unserialize Pop Chain | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/PHP-Unserialize-Pop-Chain) |
| 93 | SQL Injection - Second Order | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-Injection-Second-Order) |
| 94 | Python - dotenv | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Python-dotenv) |
| 95 | Python - Blind SSTI Filters Bypass | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Python-Blind-SSTI-Filters-Bypass) |
| 96 | XPath injection - Blind | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/XPath-injection-Blind) |
| 97 | SQL injection - Filter bypass | ⚪ Sin documentación; pendiente de resolución | [reto oficial](https://www.root-me.org/en/Challenges/Web-Server/SQL-injection-Filter-bypass) |

## Otras categorías — retos validados y documentados

### App - Script — orden del catálogo

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | Bash - System 1 | ✅ Validado y documentado | [writeup](challenges/app-script/bash-system-1/README.md) |

### Cracking — orden del catálogo

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | ELF x86 - 0 protection | ✅ Validado y documentado | [writeup](challenges/cracking/elf-x86-0-protection/README.md) |
| 2 | ELF x86 - Basic | ✅ Validado y documentado | [writeup](challenges/cracking/elf-x86-basic/README.md) |
| 3 | PE x86 - 0 protection | ✅ Validado y documentado | [writeup](challenges/cracking/pe-x86-0-protection/README.md) |
| 4 | ELF C++ - 0 protection | ✅ Validado y documentado | [writeup](challenges/cracking/elf-cpp-0-protection/README.md) |

### Cryptanalysis — orden del catálogo

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | Encoding - ASCII | ✅ Validado y documentado | [writeup](challenges/cryptanalysis/encoding-ascii/README.md) |
| 2 | Encoding - UU | ✅ Validado y documentado | [writeup](challenges/cryptanalysis/encoding-uu/README.md) |
| 6 | Hash - Message Digest 5 | ✅ Validado y documentado | [writeup](challenges/cryptanalysis/hash-md5/README.md) |
| 8 | Hash - SHA-2 | ✅ Validado y documentado | [writeup](challenges/cryptanalysis/hash-sha-2/README.md) |

### Network — orden del catálogo

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | FTP - authentication | ✅ Validado y documentado | [writeup](challenges/network/ftp-authentication/README.md) |
| 2 | TELNET - authentication | ✅ Validado y documentado | [writeup](challenges/network/telnet-authentication/README.md) |
| 3 | ETHERNET - frame | ✅ Validado y documentado | [writeup](challenges/network/ethernet-frame/README.md) |
| 6 | Twitter authentication | ✅ Validado y documentado | [writeup](challenges/network/twitter-authentication/README.md) |

### Web - Client — orden del catálogo

| # | Reto | Estado | Writeup |
|---:|---|---|---|
| 1 | HTML - disabled buttons | ✅ Validado y documentado | [writeup](challenges/web-client/html-disabled-buttons/README.md) |
| 2 | Javascript - Authentication | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-authentication/README.md) |
| 3 | Javascript - Source | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-source/README.md) |
| 4 | Javascript - Authentication 2 | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-authentication-2/README.md) |
| 5 | Javascript - Obfuscation 1 | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-obfuscation-1/README.md) |
| 6 | Javascript - Obfuscation 2 | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-obfuscation-2/README.md) |
| 7 | Javascript - Native code | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-native-code/README.md) |
| 9 | Javascript - Obfuscation 3 | ✅ Validado y documentado | [writeup](challenges/web-client/javascript-obfuscation-3/README.md) |
| 10 | XSS - Stored 1 | ✅ Validado y documentado | [writeup](challenges/web-client/xss-stored-1/README.md) |

## Bitácora de validación y documentación

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
| 2026-10-29 | GraphQL - Introspection | Resuelto mediante introspección del esquema GraphQL; la palomita y el «Like» fueron confirmados. | [web-server/graphql-introspection](challenges/web-server/graphql-introspection/README.md) |

## Criterio de registro

- Un writeup cuenta como documentado cuando explica el reto de forma reproducible y no incluye flags ni credenciales. Las validaciones nuevas se resuelven en el orden del catálogo y se registran también en Root-Me.
- Las cantidades del catálogo y las validaciones de la cuenta se obtienen desde [Root-Me Challenges](https://www.root-me.org/en/Challenges/) en inglés, que es la fuente de verdad de este seguimiento.
- Los retos que ya aparezcan resueltos en la cuenta se registrarán por separado de los writeups pendientes, para no confundir progreso en plataforma con documentación local.
