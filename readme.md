![](https://github.com/david-garcia-sec/OverTheWire-Bandit-Notes/blob/7ddd862895a1d0ea244b3cfb1ba19400418d0652/images/otw-bandit.jpg)
# OverTheWire-Bandit-Notes
El nivel "bandit" en OverTheWire.org (https://overthewire.org/wargames/bandit/) es conocido en ciberseguridad por ofrecer al usuario un conocimiento decente con ssh, permisos, redirecciones y pipes. Mi objetivo con este repo es reforzar ese conocimiento para poder trabajar con más soltura en SOC L1.

*Cada vez que superemos un nivel es una buena práctica guardar la pass de cada uno en un .txt.*
*Cuando no sepamos usar un comando podemos usar ``man`` ``-h`` o ``--help``.
Por ejemplo:

## Nivel 0
En este nivel solo nos enseñan a conectarnos por ssh a la máquina objetivo.

Host: bandit.labs.overthewire.org
Puerto: 2220

Para usar ssh usaremos:

``ssh usuario@host -p 2220`` con -p especificamos el puerto.

``ssh bandit0@bandit.labs.overthewire.org -p 2220`` y de contraseña cuando nos la pida ``bandit0``


En los siguientes niveles será banditX según el nivel y de pass una string de texto que encontremos en el directorio con más o menos dificultad, por ejemplo:

``ssh bandit4@bandit.labs.overthewire.org -p 2220``

Y cuando nos pida la password será una string de texto como:

``aBNSDUGHBSjdbsadyuhsandskansj``

## Nivel 1

