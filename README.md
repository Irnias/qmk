# QMK - teclado Rama

### Instrucciones de instalacion
1. Descargar QMK Toolbox (Para formatear firmware). ```https://github.com/qmk/qmk_toolbox/releases```
2. Clonar repositorio de qmk:
``` 
git clone https://github.com/qmk/qmk_firmware.git
```
3. Navegar hasta keymaps
```
cd qmk_firmware/keyboards/crkbd/keymaps
```
4. Clonar este repositorio dentro de una nueva carpeta llamada ram:
```
git clone git@github.com:Irnias/qmk.git ram
```
5. Volver a la carpeta raiz *qmk_firmeware*
```
cd ..
cd ..
cd ..
```
6. Opcional para limpiar firmeware, sino saltar al paso 7:
    * Abrir QMK Toolbox,
    * conectar una de las dos partes del teclado via usb-c
    * Precionar el boton fisico de reset en ese teclado
    * En la aplicacion hacer click sobre el boton que dice "Clear EEPROM"
    * Repetir proceso en la otra parte del teclado.
    
7. Una vez en la terminal estemos dentro de la raiz:
   * Ejecutamos el siguiente comando:
   ```
    make crkbd/rev1:ram:dfu
   ```
   * Cuando termine de compilar pedira conectar uno de las dos partes del teclado.
   * Conectar y apretar el boton fisico de reset.
   * Repetir con la otra parte del teclado.

### Instrucciones de actualizacion de teclas:

Dentro de este repo se encuentra el archivo keymap.c el cual se tiene que editar para sobreescribir la configuracion que se utilizara en el proceso.
