# Practica 1 - Sistemas Operativos 2
## 1-. Diferencias entre HDA, SDA y VDA 
-
-
-

## 2-. ¿Cómo montar y desmontar un usb en el sistema, por medio de una terminal?
Para poder montar un dispositivo (incluyendo USBs), se utiliza el comando `sudo mount [sistema de archivos] -o rw, umask=[número de umask] [dispositivo a montar] [carpeta donde se montará]`.

## 3) Enlistar la información de los dispositivos de bloque conectados, aunque no estén montados en terminal:
Para poder enlistar la información de los dispositivos de bloque conectados, estén montados o no, se utiliza el comando `lsblk`.

![](https://github.com/TavSc/Practica-1-SO2/blob/2c1ab760ede9c5d95defc98a9a2c610ca69920b7/Im%C3%A1genes/3.png)

## 4) Mostrar la tabla de particiones del disco donde está instalado el sistema operativo en terminal:
Para mostrar la tabla de particiones del disco donde está instalado el sistema, se utiliza el comando `fdisk -l` , con privilegios de superusuario (utilizando el prefijo `sudo`).

![](https://github.com/TavSc/Practica-1-SO2/blob/5d9ce2af346b9bb1e558ae0bc252d781aa8f0f28/Im%C3%A1genes/4.png)

## 5) Desplegado de las particiones de una USB en terminal:

## 6) Borrado de las particiones de una USB en terminal: