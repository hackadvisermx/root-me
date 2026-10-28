# Web - Client — Javascript - Native code

## Descripción

- **Dificultad:** Medium
- **Puntos:** 15
- **Reto:** [Root-Me — Javascript - Native code](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Native-code)

El script se presenta como una función autoejecutable y ofuscada. El depurador del navegador permite detener la ejecución y observar el código o valor ya reconstruido.

## Solución

1. Cancelar el cuadro inicial y abrir DevTools.
2. Colocar un breakpoint en el script o quitar temporalmente la invocación final de la función autoejecutable en una copia de análisis.
3. Avanzar hasta la función que devuelve el valor decodificado; alternativamente, inspeccionar la función con `toString()` cuando resulte aplicable.
4. Usar el resultado solo en Root-Me.

## Estado de revalidación

La cuenta conserva la validación y se registró el «Like». La instancia anterior no ofrece ya el script original, por lo que se documenta la reconstrucción de la técnica sin el valor recuperado.

## Notas adicionales

- El código que debe ejecutarse en un cliente puede inspeccionarse y depurarse allí.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Client/Javascript-Native-code)
- [MDN — Function.prototype.toString](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/toString)
