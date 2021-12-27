# Manipulando texto en Vim

Editar texto de una manera ágil, eficiente y precisa es una de las mejores habilidades que puede tener un administrador de sistemas o un programador, ya que te facilita y te hace ganar mucho tiempo a la hora de desarrollar tus aplicaciones y editar o crear tus ficheros de configuración.

En este escanrio, veremos como podemos editar y manipular texto con el editor Vim que nos dara esa eficiencia y agilidad a la hora de crear y editar nuestros ficheros.

Asi que **¡¡Comencemos!!** :wink:


## Insertary añadir texto y lineas, copiar y pegar texto y lineas, eliminar texto y lineas.

Vamos a crrear nuestro fichero de pruebas copiandonos la ayuda de vim.

1. Abrimos nuestro editor Vim:
```bash
vim
```
2. Creamos nuestro fichero de pruebas:
```vim
:help
:w ~/ficheropruebas.txt
:q
:e ~/ficheropruebas.txt
```
3. Vamos al principio de nuestro fichero ```gg``` y navegamos hasta la llinea que comienza con:
```
Get out of Vim
```
4. Pulsamso la tecla ```o``` para abrir una nueva linea de texto y pasarnos al **Modo Insertar**
5. En la linea que acabamos de abrir ponemos el siguiente texto:
```
ATENCIÓN: ¡¡A partir de hoy no uses otro editor distinto de VIM!! 
6. Cuando la tengas escrita pulsa la tecla ```ESC``` para salir al **MOdo Comando**
7. Ubica el cursor en una linea vacia entre tu linea actual y otra que pone ```Jump to a subject```, elimina la linea vacia pulsando ```dd```
8. Ahora vamos a copiar la linea que hemos escrito nosotros, para ello vamos a navegar hasta la linea que hemos escrito y vamos a pulsar ```yy``` para copiar esa linea.
9. Muevete ahora a la linea que empieza con ```Jump Back``` y pulsa la tecla ```p``` para pegar la linea que hemos copiado justo debajo de la linea que estamos ubicados.
10. Ubica tu cursor en la linea actual y la que hay entre la linea que empieza ```Get specific help``` y presiona la tecla ```yy``` para copiar una linea en blanco.
11. Ahora vamos a crear lineas vacias por encima de donde esmos ubicados pulsando ``P``
12. Ahora vamos a crear lineas que comiencen con un rango de números usando el siguiente comando:
```vim
:put =range(1,10)
```
**NOTA:**De este modo ganamos tiempo para hacer listados ya que podemos poner el rango que necesitemos :wink:

# Seleccionar, copiar, y pegar texto con el MODO VISUAL, deshacer cambios y rehacer cambios

**NOTA:**Para poder seguir esta parte del laboratorio debes haber realizado la parte anterior

1. Posiciona tu cursor en el número ```4``` de la lista que acabamos de crear, y copia y pega esa linea con:
```vim
yy
p
```
2. Ahora situandonos en el último 4 seleccionamos desde ahí hast el número 10 haciendo lo siguiente:
```vim
CTRL + v
CURSOR HACIA ABAJO (hasta que selecionemos el número 10)
```
3. Ahora incrementamos esos numeros pulsando con ```CTRL + a``` para que el 4 de tu cursor sea el 5 y la lista termine en 11.
4. Mueve tu cursosr hasta la linea que pone 1.
5. Selecciona las lineas numeradas del 1 al 9 pulsando:
```vim
CTRL + v
8j
```
 
