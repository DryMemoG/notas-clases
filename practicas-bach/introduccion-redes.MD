# Introducción a las Redes

> Las redes de internet son un conjunto de dispositivos electrónicos, programas y sistemas que se interconectan para permitir la transmisión y recepción de información a través de la red global de computadoras llamada Internet.
>
> La red de Internet se basa en el protocolo de comunicación TCP/IP (Transmission Control Protocol/Internet Protocol) y funciona como una gran red de redes, interconectando millones de dispositivos en todo el mundo, desde computadoras personales y servidores hasta teléfonos inteligentes, tabletas y otros dispositivos electrónicos.
>
>  Las redes de Internet permiten a los usuarios conectarse a servidores y recursos remotos, enviar y recibir correo electrónico, chatear con amigos y familiares, realizar compras en línea, descargar y compartir archivos, y acceder a una amplia variedad de contenido multimedia, como videos, música y juegos.
>
> En resumen, las redes de Internet son la infraestructura fundamental que permite la comunicación y el intercambio de información en todo el mundo, conectando a personas y dispositivos de todo tipo a través de la red global de computadoras conocida como Internet.

## **Conceptos Fundamentales (Lógicos):** 
___
### **1. Red de Área Local (LAN):** 
Una red local *(Local Area Network)* es una red de computadoras que abarca un área reducida, por ejemplo una casa, el laboratorio de computación o un edificio. 

### **2. Red de Área Amplia (WAN):**
Esta red de área amplia *(Wide Area Network)* es uyna red que une varias redes locales, generalmente sus mienbros no están en la misma ubicación física. 
### **3. Subred:** 
Una subred es un rango de direcciones lógicas. Cuando una red de computadoras se vuelve muy grande conviene dividirla en subredes, esto se hace para reducir el tamaño de los dominios de [broadcast](https://www.ionos.es/digitalguide/servidores/know-how/broadcast/), hacer la red mas manejable, etc. 
### **4. Internet:**
Internet es un conjunto descentralizado de redes de comunicación interconectyadas que utilizan la familia de protocolos TCP/IP lo cual garantiza que las redes físicas heterogéneas que la componen formen una red lógica única de alcance mundial. 

### **5. Protocolo TCP/IP:**
El protocolo TCP/IP son un conjunto de reglas que permiten la comunicación de las computadoras mediante la Red, se basan en la dirección IP. Cada computadora conectada a una red o a internet, tiene que tener asignada una única IP para estar identificada en la red. 
### **6. Dirección IP:**
Las direcciones IP *(Internet Protocol)* son una serie de números que identifican de manera única a cada dispositivo conectado a una red de internet. Las direcciones IP se dividen en dos partes principales: la primera parte identifica la red a la que está conectado el dispositivo y la segunda parte identifica al dispositivo dentro de esa red. Aquí un ejemplo de como se ve una dirección IP
```console
Dirección IPv4...........: 192.168.1.10
```
```code
:\\192.168.2.10
```
Dicha dirección es necesaria para que los dispositivos puedan comunicarse entre sí en una red de internet.

### **7. Máscara de [subred](https://es.wikipedia.org/wiki/M%C3%A1scara_de_red):**
La IP por si sola no es suficiente para identificarte dentro de la red, por lo que falta una segunda IP que determine las partes fijas de la primera. A efectos prácticos se trata de otra dirección IP pero que casi siempre va a estar compuesta por ceros y 255's. 
El 255 indica que la dirección no varía, mientras que el 0 representa a los que van a variar. Un ejemplo sería el Siguiente: 
```console
Dirección IP 1: 192.168.0.1
Máscara de Subred: 255.255.255.0
Dirección IP 2: 192.160.1.10
Máscara de Subred 255.255.255.0
```
Simplificando bastante podríamos decir que las partes fijas de la IP representan la red que uno tiene para conectarse a internet, mientras el número variable se usa para que las computadoras puedan determinar si las direcciones a las que se van a conectar están en la red local o en una remota. 

## **Conceptos Fundamentales (Hardware):**







