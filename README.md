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