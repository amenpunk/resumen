Diagramas a memorizar:
* OSI
* Clase de ipv4 Privdadas(Ip inicial, Ip Final)

![](https://www.google.fi/url?sa=i&source=images&cd=&ved=2ahUKEwi0k83I3fHjAhXBx1kKHUuRCroQjRx6BAgBEAQ&url=http%3A%2F%2Falejollagua.blogspot.com%2F2012%2F12%2Fnube-dispositivo-de-capa-1-7.html&psig=AOvVaw2mH1NvoUA_p-t8W1Qf0CFF&ust=1565300673746883)

# Redes Modulo 1


## Link (enlace)
Es el nivel más bajo de una red consiste dos o mas computadoras conectadas travéz de un medio fisico.

## Nodo
Cada dispositivo conectado a una red

## Enlace con Acceso Múltiple
Más de dos nodos comparten el mismo enlace


## Clasificacion de las redes.
* Redes de área personal (PAN)
* Redes de área local (LAN)
* Redes de área metropolitana (MAN)
* Redes de área amplia (WAN)
* Interredes

## Tecnologías de transmisión
* Broadcast
* Punto a Punto

## Broadcast
Todas los nodos comparten el canal de comunicación

## Punto a Punto
Conectan dos pares individuales de maquinas.

## Conmutacion de paquetedes
Muchas rutas pueden usarse para una sola comunicacion, mientras los paquetes individaules se enrutan a un destino.

## Como se comunican los mensajes
Los datos se envían a través de la red en pequeños bloques llamados segmentos.

## PDU (Unidad de datos de protocolo)
se utilizan para el intercambio de datos entre unidades disparejas, dentro de una capa del modelo OSI. 

## Diferencias entre OSI/TCP/IP
* Los protocolos TCP/IP son los estandares en torno a los cuales se desarollo la internet, de modo que la crediblidad del modelo TCP/IP se debe en gran parte a sus protocolos.
* Por lo general el modelo OSI se utiliza como guia para el desarollo de redes.

## Red Móvil 2G
Fue la primera que permitio acceder a internet a travéz del protocolo TCP/IP

## Redes 802.11
Son todas las redes compuetas por conexiones inalámbricas

## Las topologías se dividen en:
* Física 
* Lógica

## Tipos de topologia de Ethernet
* Topología de bus
* Topología de estrella
* Topología de Anillo
* Topología de Arbol
* Topología de Malla
* Topología de Doble anillo y Mixta

## Protocolos y capas que definene Ethernet
La capa Física y la de enlace de datos son las que conforman ethernet.

## Direccion MAC (Control de acceso al medio)
Es el encargado de la encapsulacion de los datos, delimitacion de tramas, direccionamiento y deteccion de errores.

## CSMA/CD (Carrier Sense Multiple Acces / Colision Detect)
Es un protocolo que permite Oir antes de hablar y hablar solo cuando los demas callan,
si mientras habalmos oimos que otro habla nos callamos este funciona en redes Ethernet su variante es CSMA/CA para redes inalambricas,este en si regula el control de acceso al medio compartido.

## Como se compone una trama Ethernet
Mac destino,mac origen, ip destino e ip origen, datos del usuario y el trailer

## proceso ARP (Resolucion de direcciones)
(ARP, del inglés Address Resolution Protocol) es un protocolo de comunicaciones de la capa de red responsable de encontrar la dirección de hardware (Ethernet MAC) que corresponde a una determinada dirección IP

## Funcion de la capa de enlace
Regulan cómo se da formato a una trama para utilizarla en diferentes medios, es posible que distintos protocolos se encuentren en uso para diferentes medios, en cada salto a lo largo de la ruta un dispositivo intermedio acepta tramas de un medio la desencapsula y luego envia los paquetes en una nueva trama, los encabezados de cada trama se formatean para el medio especifico que cruzará

## Control de enlace lógico (LLC)
Control de enlace lógico LLC ("Logical Link Control") define la forma en que los datos son transferidos sobre el medio físico, proporcionando servicio a las capas superiores.
este controla
* maneja el control de errores
* control del flujo
* entramado
* control de diálogo
* direccionamiento de la MAC.

## Algunos protocolos y estandares utilizados por la capa de enlace de datos
LLC,Ethernet,Token Ring,Wireless,HDLC

## Tecnicas de control de acceso al medio
* Full duplex
* Half duplex

## El protocolo ip (Internet Protocol)
Es un protocolo de la capa de red no orientado a conexión, el emisior no sabe si el receptor estara presente, si llegó la carta, y si el receptor puede leer la carta, el receptor no sabe cuando llegará
* ip no garantiza la recepcion de todos los paquetes enviados
* otros protocolos administran el proceso de seguimiento de paquetes.
* Los paquetes ip pueden trasladarse atravez de diferentes medios.

## Unidad de datos de protocolo(PDU)
Las unidades de protocolo de datos, también llamadas PDU (del inglés Protocol Data Unit), se utilizan para el intercambio de datos entre unidades disparejas, dentro de una capa del modelo OSI. 

## Ip clase A
Los primeros 8 bits representan la red, los restantes 24 representan el host

## IP classe B
Primeros 16 bits representan la red,los restantes 16 representan el host

## Ip clase C
Los primeros 24 bits representan la red y los restantes 8 representan el host

## Mascaras de red
Representan el numero de bits que representan a la red y la cantidad de bits que representan al host segun la clase de su IP

## Paquete IP
En redes basadas en Tcp/ip, La PDU de la capa de red es el paquete ip

## Funcion del gateway
los hosts ip desconocen como entregar los datos a los dispositivos en una red remota o dividida y esta es la funcion del gateway, 

## Paso para el enrutamiento ip
* El router elimina la encapsulacion de la capa 2
* el router extrea la ip de destino
* el router verifica la tabla de enrutamiento para detectar una con concidencia.
* se encuentra la red en la tabla de enrutamiento
* El router vuelve a encapsular el paquete
* se envia el paquete a la red

## tipos de enrutamiento
* Enrutamiento dinámico
* Enrutamiento estatico

## Asignacion de una ipv4 a un host
Esta se realiza por  medio de un DHCP

## Tipos de comunicacion en una red ipv4
* Unicast:
Proceso por el cual se envía un paquete de un host a un host individual
* broadcast:
Proceso por el cual se envía un paquete de un host a todos los hosts en la red
* Multicast:
proceso por el cual se envía un paquete de un host a un grupo seleccionado de hosts, posiblemente en redes distintas

## Direcciones privadas
Los hosts que no requieren acceso a internet pueden utilizar direcciones privadas

## Uso especial de ipv4
* No es posible asignar a un host la primera ni la ultima direccion de cada red
* La direccion 127.0.0.1 es una direccion especial que redirige el trafico a sí mismo.

## CIDR (enrutamiento entre dominios sin clase)
Este permite asignar direcciones ipv4 en cualquier limte de bits de direccion en lugar de solo con direcciones clase A,B,C

## Registro regionales de internet(RIR)
Es una organización que supervisa la asignación y el registro de recursos de números de Internet dentro de una región particular del mundo. Los recursos incluyen direcciones IP (tanto IPv4 como IPv6) y números de sistemas autónomos (para su uso en encaminamiento BGP).

## Coexitencia de Ipv4 e Ipv6
* Dual-stack: permite que ipv4 e ipv6 coexistan en la misma red. Los dispositivos ejecutan stacks de protocolos ipv4 e ipv6 de manera simultánea.
* Tunneling: Método para trasportar paquetes ipv6 atraves de redes ipv4. El paquete ipv6 se encapsula dentro de un paquete ipv4
* Traduccion: Un paquete ipv6 se traduce en un paquete ipv4 y viceversa. 

## Tipos de direcciones Ipv6
* Unicast
* Multicast
* Anycast

## Protocolo de control de mensajes de Internet (ICMP)
es parte del conjunto de protocolos IP. Es utilizado para enviar mensajes de error e información operativa indicando, por ejemplo, que un host no puede ser localizado o que un servicio que se ha solicitado no está disponible, este esta disponible en ipv4 e ipv6
