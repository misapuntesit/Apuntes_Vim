# Laboratorio Sobrevieviendo a VIM

## ¿Eres nuevo en VIM? Relajate, con este laboratorio vas a subir más de un nivel. 
No te preocupes con este pequeño manual podrás realizar todas las acciones que realizas en cualquier editor de texto, pero con una gran ventaja, no vas a necesitar el ratón para nada :wink:

Ahora sí, abre tu terminal y preparate para disfrutar del siguiente laboratorio.
He creado el laboratorio para ir viendo paso a paso las diferentes secciones que veremos en el curso.

Si en cualquier momento te lias y no sabes como volver al punto anterior, no entres en **pánico** siempre puedes volver atrás pulsando la tecla ```ESC``` varias veces y pulsando luego la tecla ```u``` que significa **undo**, en español deshacer jejeje, o si lo prefieres puedes cerrar el fichero sin guardar los cambios pulsando la tecla ```ESC``` y luego ```:q!```

## Escenario planteado

Eres un administrador de sistemas y te encuentras que en tu nueva empresa todos los sistemas linux solo tienen instalado el editor ***VIM*** por lo que vas a necesitar aprender a usarlo si o si, no hay otra solución si no quieres el despido inmediato :laughing: .

No te queda otra que sentarte delante de tu terminal y gracias a este laboratorio obtendrás las habilidades necesarias para usar el editor Vim como un profesional y evitar que te despidan por algo tan sencillo :wink:

Te aseguro que una vez finalices este laboratorio tendrás los conocimientos necesarios para evitar ese despido. Asi que vamos al turrón...

# Crear, Abrir y Salir de un fichero

## Crear y guardar un fichero con Vim

1. Abrir Vim:

```bash
vim
```

2. Ahora nos toca insertar texto en el fichero asi que pulsa la tecla ```i``` verás que en la parte abajo a la izquierda has cambiado al **Modo Insertar**. Escribe ahora el texto que quieras tener en este fichero.

3. Una vez que tengas todo el texto escrito pulsa la tecla ```ESC``` para volver al **Modo Comando**
4. Ahora nos toca guardarlo y salir de vim para guardar el fichero en disco con el nombre 'mifichero.txt' escribiremos lo siguiente:
```bash
:w mifichero.txt

#La 'w' significa write
```

5. Ahora queremos cerrar vim para ello pulsamos:
```bash
:q

# La 'q' significa quit
```

**NOTA:** Puedes guardar y salir lanzando el siguiente comando, evitando tener que hacer el paso 4 y 5 y haciendolo en un solo paso:
```bash
:wq
```

## Editar un fichero y salir sin guardar cambios

1. Editar el fichero ```/etc/hosts ```
```bash
vim /etc/hosts
```
2. Al pulsar la tecla ```i``` entramos en el modo insercción pero nos va a dar un error ya que el fichero es de solo lectura ya que solo root puede editarlo
```bash
W10: Warning: Changing a readonly file
```
3. Intentaremos salid salir del fichero pulsando la tecla ```ESC``` y despues la combinación de teclas ```:q```  **Este paso no funciona y no podemos salir**

4. Para forzar la salida debemos pulsar ```ESC``` y después ```:q!```


## Realizar cambios a un fichero

1. Vamos a copiar la documentación de Vim a nuestra carpeta para tener un fichero con texto

```bash
cp /usr/share/vim/vim80/doc/help.txt ~/vimhelp.txt
```
**NOTA:** El directorio vim80 puede no existir lo recomendable es que escribas 
```bash 
cp /usr/share/vim/vim #Aqui dale a la tecla TAB para que te lo autocomplete
``` 
Luego rellena el resto de la ruta /doc/help.txt


2. Editamos el fichero escribiendo:

```bash
vim ~/vimhelp.txt
``` 
3. Nos movemos hasta el texto **VIM - main help file**

**NOTA:** Para movernos por el fichero tenemos dos formas de hacerlo, más abajo tenmos mas formas de movernos por nuestro fichero agilmente.
- Con los cursores / flechas del teclado
- En caso de que nuestro teclado no disponga de las teclas cursores n os podemos mover con las teclas 

```h```  ```j```  ```k```  ```l```
	
```bash
	h -->  nos movemos a la izquierda
	j -->  nos movemos hacia abajo
	k -->  nos movemos hacia arriba
	l -->  nos movemos hacia la izquierda

		j
	h		l
		k

	#RECUERDA:para movernos por el texto debemos estar en el modo comando por lo que debes pulsar la tecla ESC 
```



4. Cambiamos la palabra VIM a Vim para ello colacomas el curso en la letra i y pulsamos ```cw``` para cambiar el resto de la palabra **im**
**NOTA:** La tecla ```c``` en modo comando nos sirve para hacer cambios por lo que nos quita la letra, palabra o linea depende de como lo mandemos y se pasa a modo inserción para poder escribir directamente.

5. Ahora pulsa ta tecla ```ESC``` para salir del modo comando
6. Ahora muevete hasta la letra i y pulsa 2 veces la tecla ~ 
**NOTA:** La tecla ~ en modo comando nos cambia la letra donde este el curso de Mayúscula a Minúscula y de Minúscula a Mayúscula 
7. Ahora navega hasta la letra h de la palabra help y pulsa 3 veces la tecla ~ covirtiendo de este modo la palabra help a mayúsculas
8. Pulsa la tecla ```ESC``` para asegurarte que vuelves al modo comando
9. Guardamos y salimos pulsando:
```bash
:wq
```

## Movernos por nuestro fichero agilmente

1. Editamos nuestra copia del fichero **vimhelp.txt**
```bash
vim ~/vimhelp.txt 
```
2. Para ir al final del fichero pulsamos ```G```
3. Subir al principio del fichero pulsamos ```gg```
4. Para movernos a la linea 15 podemos hacerlo pulsando  ```15G``` o ```:15```
5. Si queremos ir a la mitad del documento teclearemos ```50%```
6. Si pulsamos 5 veces la tecla ```w``` nos moveremos 5 palabras hacia delante
7. Si pulsamos ahora 5 veces la tecla ```b``` nos moveremos 5 palapras hacia atrás

**NOTA:** Cuando ponemos un número delante de un comando ese comando se repetira el número de veces que hallamos escrito. 

8. Si queremos ir 25 palabras hacia adelante pulsaremos ```25w```
9. Para movernos por el documento podemos usar la teclas ```h``` ```j``` ```k``` ```l``` o puedes usar los cursores.
10. Si queremos buscar una palabra pondremos ```\PALABRA_QUE_BUSCAMOS``` por ejemplo prueba a poner ```\Vim``` y después ```enter```, veras como te muetra la primera palabra 'Vim' que aparezca en el documento.
11. Si queremos buscar la siguiente palabra que coincida con nuestra búsqueda pulsaremos ```n``` y si queremos buscar la anterior palabra que coincida con nuestra búsqueda pulsaremos ```N``` asi podremos buscar la palabra o cadena de texto que estemos buscando.
12. Si queremos ir al principio de la linea pulsaremos ```0```
13. Si queremos ir al final de la linea pulsaremos ```$```
14. Pulsa ahora ```:q!``` para salir del documento sin guardar los cambios

 
## Insertar,copiar y borrar texto

1. Volvemos a editar el fichero **vimhelp.txt**

```bash
vim ~/vimhelp.txt
```
2. Navegamos al principio del fichero ```gg``` hasta la frase ```Get out of Vim```
3. Si queremos **añadir una nueva linea debajo de la linea** en la que estamos pulsamos ```o``` yo relacciono la ```o``` con 'open new line' si queremos escribir arriba de la linea que estamos pulsaremos ```O```
4. Y por ejemplo escribimos la siguiente frase ```NOTA:  Estamos aprendiendo a escribir con Vim!``` y pulsa ```ESC```
5. Para **eliminar un linea** completa pulsaremos en modo comando ```dd```
6. Ahora vamos a **copiar la linea completa** que hemos escrito para ell nos movemos hasta nuestra frase y pulsamos ```yy``` la y y viene de **yank** en ingles y ya tenemos copiada la linea
7. Ahora vamos a **pegar esa linea que hemos copiado justo debajo** pulsando la tecla ```p``` que nos la pega justo debajo de donde estabamos ubicados, si queremos **pegar la linea justo arriba** pulsaremos la tecla ```P```
8. Un truco para dejar hueco en el documento es copiar una linea en blanco, para ello vamos una linea en blanco y la copiamos ```yy``` despues vamos donde queremos dejar el hueco por ejemplo 4 lineas en blanco y pulsamos ```4p``` esto nos pega 4lineas iguales a la que habiamos copiado, como era una linea en blanco pegamos 4 lineas en blanco.
9. Si queremos eliminar una letra nos podemos mover a la letra que queremos eliminar y pulsar la tecla ```x```

**HACER CAMBIOS EN MODO VISUAL**
Podemos seleccionar texto de manera visual para ello haremos lo siguiente:

1. Pulsamos la tecla ```v```
2. Nos movemos para seleccionar las 4 lineas en blanco que acabamos de pegar y pulsamos ```d``` para eliminar esas lineas, en caso de que queramos copiar las lineas que hemos seleccionado pulsaremos la tecla ```y```
3. Si queremos seleccionar solo columnas podemos pulsar ```CTRL + V``` de este modo podemos seleccionar la columna que necesitemos copiar o eliminar siguiendo el procedimiento del punto 2.

## Deshacer y rehacer cambios

1. Para deshacer cambios salimos al modo comando con la tecla ```ESC``` y pulsamos la tecla ```u``` **undo** pulsaremos la tecla tanas veces como cambios queramos revertir.
2. Cuando llegamos al ultimo cambio posible veremos en la parte de abajo nos indica **Este es el cambio más antiguo**
3. Una vez que hemos llegado al último cambio que podemos rehacer nos parecera en la parte de abajo a la izquierda la frase **Este es el cambio más nuevo**

## Guardar y/o salir

1. Guardar nuestros cambios en el mismo fichero sobreescribiendolo
```bash
:w
```
2. Guardar nuestros cambios en un fichero diferente
```bash
:w ~/nuevo_fichero.txt
```
4. Podemos ver en que buffer nos encontramos pulsando 
```bash
CTRL + g
```
3. Confirmammos que solo tenemos un buffer de cambios, y que este buffer es el de nuestro fichero, e icncluye cambios:
```bash
:ls
```
4. Salir de vim sin guardar los cambios, forzamos la salida sin guardar nada:
```bash
:q!
```

## Recursos para obtener ayuda sobre vim

1. Ejecutamos vim sin abrir ningún fichero
```bash
vim
```
2. En modo comando tecleamos ```:help``` para entra en el modo ayuda
3. Si presionamos ```q``` para salir nos parecera el mensaje **grabando @q** NO hay que preocuparse puedes volver a pulsar ```q``` y para salir del modo ayuda pulsamos ```:q```
4. si queremos obtener ayuda sobre como navegar por vim podemos usar ```:h motion``` que nos lleva a la sección de la ayuda donde se explica como movernos con vim.
5. Si queremos mover una página hacia arriba y nuestro teclado es compacto y no tiene las teclas ```Page Down``` podemos usar la combinación ```CTRL + f``` la f de **forward** o para ```Page Up``` la combinación ```CTRL + b``` la b de **back**
6. El directorio donde se encuentra la documentación de vim esta en:
```bash
cd /usr/share/vim/vim80/doc
```

**NOTA:** Recuerda que el directorio **vim80** puede ser **vim81** o **vim82** dependera de tu SO. Puedes tabular cuando llegues a vim8 para que te lo autocomplete.

7. Si queremos editar el fichero visual.txt e ir directos a la linea 289 o la linea que tu elijas puedes hacerlo con:
```bash
vim +289 visula.txt
```
8. Si necesitas buscar una palabra en el fichero visual.txt puedes hacerlo así, **NOTA:** Nos dara un mensaje que estamos en un fichero de solo lectura, pulsa ```enter``` y continua:
```bash
vim +/motion visual.txt

#Nos buscara la palabra motion dentro del fichero visual.txt, recuerda que con la tecla ```n``` y ```N``` encontraremos la siguiente o anterior coincidencia.
```

## Enhorabuena, ya puedes trabajar en tu empresa con Vim moviendote como pez en el agua :wink:

