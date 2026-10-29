# Web - Client — AST - Deobfuscation

## Descripción

- **Reto:** [Root-Me — AST - Deobfuscation](https://www.root-me.org/en/Challenges/Web-Client/AST-Deobfuscation)

El recurso del reto es un árbol de sintaxis abstracta (AST) que contiene una estructura deliberadamente inválida para impedir una regeneración directa del código.

## Solución

1. Descargar el AST JSON publicado por el reto.
2. Recorrer sus nodos y detectar el nodo señuelo que no pertenece al conjunto ESTree.
3. Eliminar únicamente ese nodo inválido de la lista de expresiones; conservar el resto del árbol.
4. Regenerar JavaScript a partir del AST saneado y ejecutarlo en un entorno local aislado que capture la salida de `console`.
5. Usar la salida final exclusivamente en el formulario de validación de Root-Me.

## Verificación

La reconstrucción se realizó sobre el recurso oficial. La palomita y el «Like» se confirmaron en Root-Me; el valor de validación no se guarda en el repositorio.

## Notas adicionales

- Un AST serializado puede transportar lógica completa aunque no distribuya el código fuente original.
- La validación de tipos de nodo es esencial antes de pasar un AST a una herramienta de generación o ejecución.

