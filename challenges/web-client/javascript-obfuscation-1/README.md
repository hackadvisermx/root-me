# Web - Client — Javascript - Obfuscation 1

## Descripción

- **Dificultad:** Easy
- **Puntos:** 10
- **Reto:** [Root-Me — Javascript - Obfuscation 1](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-1)

El valor de validación está transformado en código JavaScript del lado cliente. La ofuscación dificulta la lectura, pero no impide recuperar el contenido entregado al navegador.

## Solución

1. Copiar el script a una vista formateada, sin ejecutarlo fuera de la instancia autorizada.
2. Identificar transformaciones simples de cadenas como escapes, `unescape` o conversiones numéricas.
3. Evaluar o decodificar únicamente la transformación necesaria en DevTools y recuperar el valor para Root-Me.

## Estado de revalidación

La cuenta mantiene este reto validado y su «Like» fue registrado. El artefacto original ya no está disponible en la instancia histórica; el método se conserva como reconstrucción retroactiva.

## Notas adicionales

- La ofuscación no es un control de seguridad ni una forma de ocultar secretos.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-1)
- [OWASP — Obfuscation](https://owasp.org/www-community/controls/Obfuscation)
