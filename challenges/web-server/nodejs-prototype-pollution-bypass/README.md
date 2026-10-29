# Web - Server — NodeJS - Prototype Pollution Bypass

## Descripción

- **Puntos:** 45
- **Reto:** [Root-Me — NodeJS - Prototype Pollution Bypass](https://www.root-me.org/en/Challenges/Web-Server/NodeJS-Prototype-Pollution-Bypass)

La aplicación fusiona objetos de petición con configuración interna. El filtro bloquea una forma habitual de contaminar prototipos, pero no todas las rutas equivalentes hacia el prototipo de los objetos JavaScript.

## Solución

1. Identificar el parámetro que se fusiona con la configuración y confirmar el comportamiento con una propiedad no sensible.
2. Revisar qué claves se bloquean y probar, en una cuenta de prueba, la ruta alternativa de constructor/prototipo admitida por el parser.
3. Establecer una propiedad de bajo impacto que la aplicación consulte como valor por defecto y comprobar que el cambio se hereda.
4. Limitar la contaminación al mecanismo de autorización del reto, validar el resultado en Root-Me y registrar el «Like».

## Estado de revalidación

La ruta alternativa para *prototype pollution* fue corroborada con material público. Falta reproducirla en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- Bloquear únicamente `__proto__` es insuficiente; se deben rechazar rutas peligrosas durante el parseo y la fusión profunda.
- Preferir objetos sin prototipo para diccionarios y bibliotecas de fusión actualizadas.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/NodeJS-Prototype-Pollution-Bypass)
- [OWASP — Prototype Pollution Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Prototype_Pollution_Prevention_Cheat_Sheet.html)
