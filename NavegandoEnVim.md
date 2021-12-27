# Navegación por Vim

En este apunte vamos a ver como nos podemos mover agilmente por un documento utilizando Vim y sin tocar nuestro ratón.
Empezaremos con los movimientos básicos e iremos avanzando con movimeitos que nos daran una mayor velociadad a la hora de editar nuestro documento.

Asi que **¡¡Comencemos!!** :wink:

## Movernos por vim, cambiar el cursor de posición y navegar por los buffers.

1. Abrir Vim
```bash
vim
```
2. Creamos un fichero con el que poder trbajar:
```vim
:help quotes
:w ~/mificheronavegacion.txt
```
3. Cuando lo tengamos guardado en disco podemos salir de la ayuda:
```vim
:w
```
4. Abrimos nuestro fichero ~/mificheronavegacion.txt en un buffer
```vim
:e ~/mificheronavegacion.txt
```
5. Navegamos al inicio del fichero:
```vim
gg
```
6. Navegar al final de nuestro fichero:
```vim
G
```
7. Ir a la linea número 100
```vim
100G
```
8. Ir a la mitad del fichero 50%:
```
50%
```
9. Para ver si la primera linea que vemos en la pantalla es la primera del parrafo pulsamos ```vim H``` y luego con ```vim k``` subimo una linea para asegurarnos.
10. Reposicionamos nuestro cursor en la **mitad de nuestra pantalla** (no del documento)  pulsando ```vim M``` si queremos ir a la **última linea de nuestra pantalla** pulsamos ```vim L```
11. Si ahora queremos ir a la linea 17 pulsamos ```vim 17G```
12. si pulsamos ```vim SHIFT + o``` nos abre una nueva linea encima de donde estaba nuestro cursor y se cambaia al **Modo Insertar** si ahora probamos a teclear las teclas que hemos pulsado antes para movernos por el documento, veremos que estas se estan escribiendo en el documento y no nos movemos por el documento por que ahora estamos en **Modo Insertar** 
13. Mientras estamos en el modo insertar nos podemos mover por el documento usando nuestros cursores o las teclas ```avPag, rePag, Inicio, Fin```
14. Salimos al modo comando ```vim ESC```

# Mostrar carácteres de control en nuestro fichero, Nvegar por las lineas, por las palabras y por los carácteres.

En esta sección aprenderemos a mostrar carácteres especiales que nos ayudan a saber en que linea nos encontramos si tenemos espacios o tabulaciones y también aprenderemos a movernos por la linea en la que estamos y por las palabras.

¡¡Vamos a ello!!

1. Vamos al principoio de nuestro fichero
```vim
gg
```
2. Mostramos el número de linea en la parte de la izquierda:
```vim
:set number
```
4. Si queremos ir a la primera linea del cuarto parrafo pulsaremos en modo comando:
```vim
}}}}j
````
5. Tu cursor se abra ubicado en el primer carácter de la linea que empieza:
```vim
Vim is so much better than vi...
```
6. Pulsa la tecla ```SHIFT + 4``` que es la tecla del ```vim $``` para ir al final de la linea
7. Mostrar los carácteres "extraños" que no se imprimen por pantalla como pueden ser los espacios, tabulaciones, retornos de carro, etc...
```vim
:set list
```
8. Puedes ver como el carácter ```$``` o ```LF``` (Line Feed) esta al final de cada una de las lineas, indicando el uso de un ```ENTER``` manual
9. Ubica tu cursor en la linea de arriba del parrafo que empieza con:
```
Coming with a very GUI mindset....  ```
10. Con el curaor al comienzo del parrafo, pulsa ```vim SHIFT + j``` o lo que es lo mismo la mayúscula ```J``` hasta que desaparezca el simbolo del ```$``` entre  ```Coming with``` y ```(JOse Fonseca)```.
11. Ahora pulsa el caracter ```$``` para ir al final de la linea, luego pulsa el caracter ```^``` para ir al principio de la linea
12. Usa la tecla 10 veces ```w``` para moverte 10 palabras hacia adelante de donde esta tu cursor.
13. Puedes usar la combinación de 'número + w' para moverte el número de ves que desees por ejemplo si pulsas ```5w``` te moveras 5 palabras hacia adelante
14. Puedes navegar al principio del parrafo pulsando ```B```
15. Puedes ver por que ocurre esto pulsando para ver la ayuda:
```vim
:h B
```
16. Puedes salir de la ayuda pulsando ```vim :q```
17. Posicionate de nuevo en la linea que pone ```Coming with a very GUI....```
18. Pulsa la tecla ```vim e``` para ir al último caracter de la palabra en la que estas ubicado, le puedes pulsar varias veces para ver como avanza tu cursor coincidiendo siempre con el último carácter de la palabra.
19. Vuleva al principio de la linea pulsando ```0``` o pulsando ```^```
20. Pulsa la tecla ```E``` para moverte al final de la palabra, luego hazlo varias veces más, esta vez te pararas en la coma despues de la palabra ```windows``` 
