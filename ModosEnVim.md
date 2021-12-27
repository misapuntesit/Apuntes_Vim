# MODOS EN VIM

En este laboratorio vamos a entender como funcionan los modos de Vim. Una de las cosas más importantes que debemos entender cuando empezamos a trabajar con el editor Vim, es en que modo nos encontramos y como salir de ese modo y volver al Modo Comando.

Despues de realizar este laboratorio, entederemos todos los modos de Vim  y sabremos como cambiar entre modos para realizar nuestras tareas muy agilmente.

Pues no esperemos más,**¡¡Comencemos!!** :wink:

## Arrancar Vim, Revisar los modos en la ayuda, practicar intercambiando los modos

1. Arrancamos el editor vim:
```bash
vim
```
2. Entramos en la ayuda a la seeción ```modes``` para estudiar los modos de vim:
```bash
:help vim-modes
```
4. Podemos ver los **Modos Básicos** que tiene Vim, también apreciamos que la yuda no es muy larga.
5. Presionaremos la siguiente combimnación de teclas para mostrar más ayuda:
```bash
CTRL + w
10+
```
**NOTA:** Con esta acción incrementaremos el tamñano de la ventana de ayuda y nos permite leer más sin tener que hacer scroll.
6. Cunado finalices la lectura de los **7 Modos Básicos**, saldremos de la ayuda presionando:
```bash
:q
```
7. Verificamos que estamos en el **Modo Comando** pulsando la tecla ```ESC``` varias veces para asegurarnos :wink: 
8. Cambiamos al **Modo Insertar** pulsando la tecla ```i``` Y escribimos la frase que queramos por ejemplo *Esta es nuestra primera frase escrita con el editor Vim* una vez escrita pulsamos la tecla ```ESC``` para volver al **Modo Comando**
**NOTA:** Cuando estas en **Modo Insertar**, en la parte de abajo a la izquierda aparece el texto ```-- INSERTAR -- ``` Que nos indica que estamos en **Modo Insertar**
9. Como el cursor esta en la linea que acabamos de escribir, vamos a seleccionar toda la linea con el **Modo Linea Visual** presionando la combinación de teclas:
```bash
SHIFT + v
``` 
10. Ahora que tenemos la linea seleccionada podemos cambiar la frase y ponerla en mayusculas pulsando la combinación de teclas:
```bash
SHIFT + u
```
11. Ahora podemos volver al **Modo Comando** pulsando la tecla ```ESC``` y guardaremos el buffer al fichero ```fichero1.txt``` para guardarlo pulsaremos:
```bash
:w fichero1.txt
```
12. Para salir del editor pulsaremos:
```bash
:q
```

**NOTA:** Si alguna ves que vim te muestra un mensaje en la parte inferior que ponga ```grabando @q```, puedes salir de ese estado pulsando la tecla ```q``` para parar la grabación. Hablaremos de la grabación en otro apuntey cuando hablemos de los buffers.


## Modo Comando

Cuando entramos en vim por defecto nos encontramos en el modo comando, esto quiere decir que si presionamos teclas, **NO ESTAREMOS ESCRIBIENDO** si no que estaremos lanzando comandos que realizaran acciones en nuestro editor.

**Por Ejemplo:** si pulsamos la tecla ```w``` moveremos el cursor a la siguiente palabra

## Seleccionar y manipular texto en el Modo Visual, volver al Modo Comando guardar y salir
 
1. Abrimos nuestro editor Vim
```bash
vim
```
2. Creamos un fichero con el que poder trabajar para ello vamos a ir a una sección de la ayuda y nos la vamos a guardar en un fichero nuestro donde podremos practicar:
```bash
:help quotes
:w ~/mifichero.txt
```
3. Cuando el fichero se haya escrito en disco, el estado nos mostrara la palabra ```[convertido]```, asi que salimos de la ayuda pulsando:
```bash
:q
```
4. Mientras continuamos en vim podemos abrir nuestro fichero en otro buffer de memoria, (como si fuese otra pestaña de un explorador) para ello pulsamos:
```bash
:e ~/mifichero.txt
```
5. Navegamos al parrafo que comienza por:
```
Coming with a very GUI mindset...
```
6. Ubicamos nuestro cursor en el primer caracter de la palabra ```Coming``` y pulsamos la tecla ```v``` para arrancar el **Modo Visual**. Abajo nos mostrar el texto ```-- VISUAL --``` indicandonos el modo en el que nos encontramos.
7. Ahora seleccionamos el texto ```Coming``` pulsando la tecla ```e``` para ir al final de esa palabra.
8. Presinamos ```w``` un par de veces para seleccionar un par de palabras más
9. Ponemos las palabras seleccionadas en mayusculas pressionando la tecla ```U``` mientras estan las palabras seleccionadas en el **Modo Visual**, en es e momento vemos como las palabras pasan a estar en mayusculas y el modo ```-- VISUAL --``` desaparece por que hemos vuelto al **Modo Comando**.
10. Entramos de nuevo al modo visual pulsando otra vez la combinación:
```
SHIFT + v
```
11. Movemos el cursor hacia abajo para seleccionar el parrafo y pulsamos la tecla ```U``` para cambiar el parrafo a Mayúsculas.
12. POdemos reseleccionar el parrafo rápidamente pulsando:
```
gv
```
14. Ahora vamos a aelimnar el parrafo seleccionado pulsando ```d``` 
15. Guardamos el fichero y salimos
```
:wq
```

# Selecionar columnas en Modo Bloque Visual

Si necesitamos realizar la misma acción sobre una columna el **Modo Bloque Visual** nos ayuda a realizarlo de una forma muy sencilla.
En este ejemplo vamos a crear un fichero con el listado de un directorio que nos muestra diferentes columnas y vamos a eliminar la columna de permisos.

1. Vamos a crearnos un fichero en el que tengamos columnas, para ello vamos a realizar un ```bash ls``` del directorio root ```/``` y nos lo vamos a guardar en un fichero de texto:
```bash
cd
ls / -al > editando_en_modo_bloque_visual.txt
```
2. Abrimos nuestro fichero:
```bash
vim editando_en_modo_bloque_visual.txt
```
3. Nos ubicamos en el primer caracter de la columna que queremos eliminar y pasamos al **Modo Bloque Visual**
```
CTRL + SHIFT + v
```
4. Nos movemos con los cursores o con las teclas ```h j k l``` seleccionando la columna que queremos elimnar
5. Una vez seleccionada la columna pulsamos la tecla ```x``` para eliminarla.

# Seleccionar lineas en Modo Linea Visual

Ahora vamos a eliminar una linea del mismo fichero que teniamos abierto en la anterior sección.

1. Navegamos con los cursores o con las teclas ```h j k l``` hasta la linea que queremos eliminar.
2. Pulsamos la combinación de teclas ```SHIFT + v```
3. Pulsamos la tecla ```d``` para elinar la fila


Y con esto ya podemos modificar nuestro ficheros muy agilmente, al principio cuesta, pero conforme vamos usando los comandos vamos ganando velocidad y el trabajo se realiza mucho más sencillo sin tocar el ratón :wink:
