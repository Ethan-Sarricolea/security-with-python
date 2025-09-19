# security-with-python
These are my notes about security and networks with python
> Estas son mis notas respecto a la seguridad y redes con python.

## Sockets

The sockets be a key piece that allow codes use the os functions for connecting to network.
> Los sockets son una pieza clave que permite a los codigos usar las funciones de los sistemas operativos para conectarse a la red.

```python
"""sockets TCP""" (socket.SOCK_STREAM)
"""sockets UDP""" (socket.SOCK_DGRAM)

s = socket.socket(socketFamily, socketType, protocol)

socket.AF_INET
socket.AF_INET6
```

We can think it as a comunication link between two points, usually one client and one server. The network sockets facilitate the data exchange between the process that may be executing on the same computer or on separated devices.
> Podemos pensar en ellos como un enlace de comunicación entre dos puntos, comunmente cliente y un server. Los sockets de red facilitan el intercambio de datos entre los procesos que pueden ejecutarse en el mismo equipo o en servicios separados.

In a network, comunication between diferent devices its carried out through the basic concept of socket. where a socket represents the terminal point of one conection, allowing programms exchange data together, even if they are found on different computers.
> En una red, la comunicación entre diferentes servicios se realiza a traves de del concepto basico de socket. Donde un socket representa el punto terminal de una conexión, permitiendo que los programas intercambien datos entre si, incluso si se encuentran en computadoras distintas

Each socket is associed with an IP addres, a specific port and a network protocol. In python, when works with sockets, we can find what is necessary within the socket module.
> Cada socket esta asociado a una direccion IP, un puerto especifico y a un protocolo de red. En python al trabajar con sockets podemos encontrar lo necesario dentro del modulo socket

There are two types of distincts sockets, those based on the TCO flow they offer safer conections, and UDP datagram sockets used for faster but less reliable communications.
> Existen dos tipos distintos de socket, los basados en el flujo TCP que ofrecen conexiones confiables y los sockets de datagramas UDP que se utilizan para comunicaciones mas rápidas pero menos fiables.

We will be learn about the TCP sockets since they cover most of the common use case.
> Aprenderemos de los sockets TCP ya que cubrem la mayor parte de los casos de uso comunes.

We can also divide the sockets according to their family, we have the Unix sockets, 
> Tambien podemos dividir a los sockets según su familia, tenemos los sockets tipo Unix, creados angtes de la aparición de redes y que operan sobre el sistema de archivos. Tambien los sockets de internet para la comunicación sobre redes cque usan el protocolo IPv4 y que permiten conexiones entre dispositivo mediante direcciones IP de 32 bits y números de puerto.

In turn, we find the sockets for IPv6 
> A su vez encontramos los sockets de internet para IPv6, los cuales permiten comunicación con direcciones IP de 128 bits.

## Practice

```python
import socket
```
