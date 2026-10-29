# Web - Server — Java - Spring Boot

## Descripción

- **Reto:** [Root-Me — Java - Spring Boot](https://www.root-me.org/en/Challenges/Web-Server/Java-Spring-Boot)

La aplicación Spring Boot deja expuesto un volcado de memoria. Ese artefacto puede retener objetos de autenticación, variables de entorno u otros valores sensibles que no deben publicarse mediante los endpoints de diagnóstico.

## Solución

1. Enumerar exclusivamente las rutas de diagnóstico de la instancia Start y confirmar si se expone el *heap dump*.
2. Descargar el volcado como recurso del reto y abrirlo localmente con una herramienta de análisis de heap, sin subirlo a servicios externos.
3. Buscar instancias de cadenas y objetos de configuración relacionados con la aplicación, empezando por los componentes de autenticación y las propiedades sensibles.
4. Verificar el valor hallado únicamente en el formulario de Root-Me y eliminar el artefacto temporal al terminar.

## Estado de revalidación

La exposición de un *heap dump* Spring Boot y el método de análisis local fueron corroborados con un writeup público. Falta ejecutarlo en la instancia Start autenticada, validar y registrar el «Like».

## Notas adicionales

- En producción, no se deben exponer `heapdump`, `env` ni endpoints Actuator sensibles a redes no confiables.
- Restringir Actuator por red y autenticación, y mantener una lista mínima de endpoints publicados.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/Java-Spring-Boot)
- [Spring Boot Actuator — Heap Dump](https://docs.spring.io/spring-boot/reference/actuator/endpoints.html#actuator.endpoints.heapdump)
