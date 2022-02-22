# Practica 1 - Sistemas Operativos 2
## 1-. Diferencias entre HDA, SDA y VDA 
-
-
-

## 2-. ¿Cómo montar y desmontar un usb en el sistema, por medio de una terminal?

### Montar USB
Para poder montar una unidad (incluyendo USBs), se utiliza el comando `sudo mount [sistema de archivos] -o rw, umask=[número de umask] [unidad a montar] [directorio donde se montará]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/f77772108087a117998155f009da29329805eb7e/Im%C3%A1genes/2.1.png)

### Desmontar USB:
Para desmontar una unidad (incluyendo USBs), se utiliza el comando `sudo umount [directorio donde se montó la unidad]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/b73b54d9e72c1003cae89fc6ae503e9e2d59fa54/Im%C3%A1genes/2.2.png)

## 3) Enlistar la información de los dispositivos de bloque conectados, aunque no estén montados en terminal:
Para poder enlistar la información de los dispositivos de bloque conectados, estén montados o no, se utiliza el comando `lsblk`.

![](https://github.com/TavSc/Practica-1-SO2/blob/48ca4597342f4594b9f27be124d768f259120b57/Im%C3%A1genes/3.png)

## 4) Mostrar la tabla de particiones del disco donde está instalado el sistema operativo en terminal:
Para mostrar la tabla de particiones del disco donde está instalado el sistema, se utiliza el comando `sudo fdisk -l`.

![](https://github.com/TavSc/Practica-1-SO2/blob/03c6b74fe8a28ec4d0136d6d74934091021f4072/Im%C3%A1genes/4.3.png)

## 5) Desplegado de las particiones de una USB en terminal:
Para mostrar la tabla de particiones una USB, se utiliza el comando `sudo fdisk -l [unidad que se requiere para mostrar sus particiones]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/12b694d981cfa8ba7ddb377cf5670bac8290f16d/Im%C3%A1genes/5.png)

## 6) Borrado de las particiones de una USB en terminal:
Para borrar particiones en una unidad (incluyendo USBs), se utiliza el programa `fdisk`. La forma de ingresar al programa, es por medio del comando `sudo fdisk [dispositivo al cúal se le van a eliminar las particiones]`. 

![](https://github.com/TavSc/Practica-1-SO2/blob/71693ad58f2ce51aaf9f1510ce0caf5a918c564f/Im%C3%A1genes/6.3.png)

>Existen varios comandos disponibles en esta utilidad, pero para el borrado de una partición, se utiliza el comando `d`.

Una vez iniciado el programa `fdisk`, hay que escribir el comando `d`, y posteriormente se le preguntará que partición desea eliminar. Al escribir el número de partición, saldrá un mensaje que la partición se ha eliminado. Hay que repetir el proceso con todas las particiones del dispositivo.

![](https://github.com/TavSc/Practica-1-SO2/blob/71693ad58f2ce51aaf9f1510ce0caf5a918c564f/Im%C3%A1genes/6.4.png)

>Los cambios que se realicen a la unidad no serán efectivos, hasta que se utilice el comando `w`, que escribe los cambios realizados en la unidad. Si no se utiliza el comando `w` al terminar de hacer modificaciones, éstas no se guardarán.

![](https://github.com/TavSc/Practica-1-SO2/blob/71693ad58f2ce51aaf9f1510ce0caf5a918c564f/Im%C3%A1genes/6.5.png)

El proceso completo se vería así:

![](https://github.com/TavSc/Practica-1-SO2/blob/71693ad58f2ce51aaf9f1510ce0caf5a918c564f/Im%C3%A1genes/6.1.png)

Para corroborar que se hicieron los cambios, podemos usar el comando `sudo fdisk -l [unidad que se requiere para mostrar sus particiones]`.

## 7) Crear en el USB 3 particiones físicas y una partición extendida en terminal:

Para crear particiones en una unidad (incluyendo USBs), se utiliza el programa `fdisk`. La forma de ingresar al programa, es por medio del comando `sudo fdisk [dispositivo al cúal se le van a crear las particiones]`. 

![](https://github.com/TavSc/Practica-1-SO2/blob/71693ad58f2ce51aaf9f1510ce0caf5a918c564f/Im%C3%A1genes/6.3.png)

Una vez iniciado el programa `fdisk`, hay que escribir el comando `n`, y posteriormente se le preguntará el tipo de partición a crear. 

Para crear una partición lógica, se escribe `p`, y para crear una partición extendida se escribe `e`. Posteriormente, se preguntará el número de partición que se creará (1-4). 

![](https://github.com/TavSc/Practica-1-SO2/blob/75c3ed639c732cda2392cba12c671ce7861604d9/Im%C3%A1genes/7.3.png)
Luego de ello, se preguntará el primer sector que se ubicará en la partición que se está creando, y después se preguntará el último sector que se ubicará en dicha partición.

![](https://github.com/TavSc/Practica-1-SO2/blob/81c7a1c997d4c3986993d841c3903f6d7b26d5a8/Im%C3%A1genes/7.4.png)

 Hay que repetir el proceso con todas las particiones que se deseen crear.

El proceso completo se ve así:

![](https://github.com/TavSc/Practica-1-SO2/blob/81c7a1c997d4c3986993d841c3903f6d7b26d5a8/Im%C3%A1genes/7.1.png)

## 8) Crear una partición dentro de la partición extendida del USB en terminal:
Para crear una partición dentro de una partición extendida, se siguen los mismos pasos que en el punto de arriba para crear particiones primarias, y la partición se guardará automáticamente en la extendida.

![](https://github.com/TavSc/Practica-1-SO2/blob/4632b701bb08e179ec259d1c5d9452e3baffb53d/Im%C3%A1genes/8.png)

## 9) Utilizando la aplicación Disks, borrar las particiones para que solo exista una partición que abarque toda la USB:

Para borrar las particiones de la unidad usando la aplicación Disks, hay que dar clic en el botón rojo ubicado en la parte derecha de la aplicación, y al apretarlo saldrá la siguiente ventana:

![](https://github.com/TavSc/Practica-1-SO2/blob/f44f31887a61c0b754b097ec5ac4e7c2198a1aff/Im%C3%A1genes/9.1.png)

Hay que apretar `Delete`, y se borrara la partición deseada. Hay que repetir este proceso para todas las particiones. Una vez se hayan borrado todas las particiones, hay que dar clic en el botón +, y se desplegará la siguiente ventana, donde se indicará el tamaño de la partición. 

>Ya que deseamos crear una partición que abarque toda la unidad, hay que dejar el valor por defecto.

![](https://github.com/TavSc/Practica-1-SO2/blob/f44f31887a61c0b754b097ec5ac4e7c2198a1aff/Im%C3%A1genes/9.3.png)

Finalmente, aparecerá una ventana, donde se tendrá que indicar el nombre de la unidad, el tipo de sistema de archivos, etc.

![](https://github.com/TavSc/Practica-1-SO2/blob/f44f31887a61c0b754b097ec5ac4e7c2198a1aff/Im%C3%A1genes/9.4.png)

## 10) Copiar un archivo ISO de distribución live de Linux a la USB, por medio del comando `dd`:

Para realizar esto, se utiliza el comando `sudo dd if=[Archivo que se desea copiar] of=[unidad destino]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/ace6f57e60afca815097c94a543148748b1dedf4/Im%C3%A1genes/10.png)