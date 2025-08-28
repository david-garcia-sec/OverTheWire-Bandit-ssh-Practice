![](https://github.com/david-garcia-sec/OverTheWire-Bandit-Notes/blob/7ddd862895a1d0ea244b3cfb1ba19400418d0652/images/otw-bandit.jpg)
# Introducción
El nivel "bandit" en OverTheWire.org (https://overthewire.org/wargames/bandit/) es conocido en ciberseguridad por ofrecer al usuario un conocimiento decente con ssh, permisos, redirecciones y pipes. Mi objetivo con este repo es reforzar ese conocimiento para poder trabajar con más soltura en SOC L1.

- Cada vez que superemos un nivel es una buena práctica guardar la pass del último nivel superado en un .txt. Lo podemos hacer con ``touch`` y ``nano`` para editar el texto del archivo.

![](https://github.com/david-garcia-sec/OverTheWire-Bandit-SOC-L1/blob/2fdfe4ef0e68ace3c62fcef3b13b1a8403ce97a8/images/touch.png)

Para salir de nano, mantenemos la tecla Control+x

![](https://github.com/david-garcia-sec/OverTheWire-Bandit-SOC-L1/blob/main/images/touch%202.png?raw=true)

Nos pedirá guardar los cambios. Simplemente ``y`` y enter.

Para ver nuestra pass en terminal le metemos un ``cat``.

![](https://github.com/david-garcia-sec/OverTheWire-Bandit-SOC-L1/blob/main/images/touch3.png?raw=true)

- Cuando no sepamos usar un comando podemos usar ``man`` ``-h`` o ``--help``.
Por ejemplo: ``man cat`` ``-h cat`` ``--help cat``. Para salir de la instrucción simplemente pulsamos ``q``.

## Índice
- [Nivel 0](#nivel-0) - Uso de ssh
- [Nivel 1](#nivel-1) - ls, cd, cat, file, du y find.
- [Nivel 2](#nivel-2)

## Nivel 0
En este nivel solo nos enseñan a conectarnos por ssh a la máquina objetivo.

Host: bandit.labs.overthewire.org
Puerto: 2220

Para usar ssh utilizaremos:

``ssh usuario@host -p 2220`` con -p especificamos el puerto.

``ssh bandit0@bandit.labs.overthewire.org -p 2220`` y de contraseña cuando nos la pida ``bandit0``


En los siguientes niveles será banditX según el nivel y de pass una string de texto que encontremos en el directorio con más o menos dificultad, por ejemplo:

``ssh bandit4@bandit.labs.overthewire.org -p 2220``

Y cuando nos pida la password será una string de texto como:

``aBNSDUGHBSjdbsadyuhsandskansj``

Esto suele llamarse ``flag`` en CTF's.

## Nivel 1

Cuando logueamos con bandit0 nos recomiendan usar varios comandos:

| Comando | Función                                                      | Ejemplo de uso                                                          |
| ------- | ------------------------------------------------------------ | ----------------------------------------------------------------------- |
| `ls`    | Lista archivos y directorios del directorio actual           | `ls -la` → Lista todos los archivos, incluyendo ocultos, con detalles   |
| `cd`    | Cambia de directorio                                         | `cd /var/log` → Va al directorio `/var/log`                             |
| `cat`   | Muestra el contenido de un archivo de texto                  | `cat archivo.txt` → Muestra el contenido de `archivo.txt`               |
| `file`  | Detecta el tipo de un archivo                                | `file imagen.png` → Dice que es un archivo PNG                          |
| `du`    | Muestra el uso de espacio en disco de archivos o directorios | `du -sh /home/usuario` → Tamaño total del directorio de manera resumida |
| `find`  | Busca archivos o directorios según criterios                 | `find /home -name "*.txt"` → Busca todos los archivos `.txt` en `/home` |

Solo será necesario hacer un ``ls`` para listar todo y un ``cat`` para ver el archivo ``readme``.

*Para terminar la sesión solo con poner ``logout`` o ``exit`` será suficiente.*

## Nivel 2

