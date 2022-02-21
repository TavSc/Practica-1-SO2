# Practica 1 - Sistemas Operativos 2
## 1-. Diferencias entre HDA, SDA y VDA 

## 2-. ¿Cómo montar y desmontar un usb en el sistema, por medio de una terminal?
Para poder montar un dispositivo (incluyendo USBs), se utiliza el comando `sudo mount [sistema de archivos] -o rw, umask=[número de umask] [dispositivo a montar] [carpeta donde se montará]`.

## 3) Enlistar la información de los dispositivos de bloque conectados, aunque no estén montados en terminal:
Para poder enlistar la información de los dispositivos de bloque conectados, estén montados o no, se utiliza el comando `lsblk`.