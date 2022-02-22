# Practica 1 - Sistemas Operativos 2
## 1-. Diferencias entre HDA, SDA y VDA 
-
-
-

## 2-. ¿Cómo montar y desmontar un usb en el sistema, por medio de una terminal?

### Montar USB
Para poder montar una unidad (incluyendo USBs), se utiliza el comando `sudo mount [sistema de archivos] -o rw, umask=[número de umask] [unidad a montar] [carpeta donde se montará]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/f77772108087a117998155f009da29329805eb7e/Im%C3%A1genes/2.1.png)

### Desmontar USB:
Para desmontar una unidad (incluyendo USBs), se utiliza el comando `sudo umount [carpeta donde se montó la unidad]`.

![](https://github.com/TavSc/Practica-1-SO2/blob/b73b54d9e72c1003cae89fc6ae503e9e2d59fa54/Im%C3%A1genes/2.2.png)

## 3) Enlistar la información de los dispositivos de bloque conectados, aunque no estén montados en terminal:
Para poder enlistar la información de los dispositivos de bloque conectados, estén montados o no, se utiliza el comando `lsblk`.

![](https://github.com/TavSc/Practica-1-SO2/blob/48ca4597342f4594b9f27be124d768f259120b57/Im%C3%A1genes/3.png)

## 4) Mostrar la tabla de particiones del disco donde está instalado el sistema operativo en terminal:
Para mostrar la tabla de particiones del disco donde está instalado el sistema, se utiliza el comando `fdisk -l [disco del cuál se quieren mostrar las particiones]` , con privilegios de superusuario (utilizando el prefijo `sudo`).

![](https://github.com/TavSc/Practica-1-SO2/blob/8efa9a984bb044b4e8e2fc462dfa5ab1649b8b73/Im%C3%A1genes/4.2.png)

## 5) Desplegado de las particiones de una USB en terminal:

## 6) Borrado de las particiones de una USB en terminal: