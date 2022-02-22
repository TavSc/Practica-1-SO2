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

Luego de ello, se preguntará el primer sector que se ubicará en la partición que se está creando, y después se preguntará el último sector que se ubicará en dicha partición.

 Hay que repetir el proceso con todas las particiones que se deseen crear.

