# MODOS EN VIM

En este laboratorio vamos a entender como funcionan los modos de Vim. Una de las cosas más importantes que debemos entender cuando empezamos a trabajar con el editor Vim, es en que modo nos encontramos y como salir de ese modo y volver al MOdo Comando.

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

**NOTA:** Si alguna ves que vim te muestra un mensjae ne la parte inferiro que ponga ```grabando @q```, puedes salir de ese estado pulsando la tecla ```q``` para parar la grabación. HAablaremos de la grabación en otro apunte.


## Modo Comando

Cuando entramos en vim por defecto nos encontramos en el modo comando, esto quiere decir que si presionamos teclas, **NO ESTAREMOS ESCRIBIENDO** si no que estaremos lanzando comandos que realizaran acciones en nuestro editor.

**Por Ejemplo:** si pullsamos la tecla ```w``` moveremos el cursor a la siguiente palabra
