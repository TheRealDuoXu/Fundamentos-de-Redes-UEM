# ﻿Semana 4
## Ejercicio 3.5.5

_Mire la página del navegador web del Cliente Web. ¿Cambió algo?_
Sí, muestra la pantalla inicial del home server

_¿Qué información se enumera en los pasos numerados directamente debajo de los cuadros In Layers y Out Layers para Layer 7?_
1. El cliente envía una solicitud http al servidor
2. El servidor recibe la solicitud http
3. El servidor envía una respuesta http al cliente
4. El cliente http recibe la respuesta del servidor. La página web se muestra en el navegador.

_¿Cuál es el valor del Dst Port para Layer 4 en la columna Out Layers ?_
Desde web server a cliente, puerto destino 80, puerto fuente 1025.
Desde cliente a we server, puerto  destino 1025, fuente 80

_¿Cual es el Dest? ¿IP para Layer 3 en la columna Out Layers?_
Desde web server a cliente, ip destino 192.168.1.254, ip fuente 192.168.1.1
Desde cliente a we server,  ip destino 192.168.1.1, ip fuente 192.168.1.254
La ip coincide con la ip de broadcast, por lo que el servidor desencapsula el mensaje.

_¿Qué información se muestra en Layer 2 en la columna Out Layers ?_
La trama coincide, por lo que procede desencapsular el encabezado ethernet

_¿Cuál es la información común que figura en la sección IP de los PDU Details en comparación con la información que figura en la pestaña del OSI Model ? ¿Con qué capa está asociado?_
SRC IP:192.168.1.254 
DST IP:192.168.1.1 
Está asociado con la capa 3

_¿Cuál es la información común que aparece en la sección TCP de PDU Details, en comparación con la información que aparece en la pestaña delOSI Model , y con qué capa está asociada?_
SOURCE PORT:80 
DESTINATION PORT:1025 
Esta asociada con la capa 4

_¿Cuál es el host que aparece en la sección HTTP de los PDU Details? ¿Con qué capa se asociaría esta información en la pestaña del MOdelo OSI?_
Server: PT-Server/5.2, esta asociada con la capa 7

_Comparando la información que se muestra en la columna In Layers con la de la columna Out Layers, ¿cuáles son las principales diferencias?_
La diferencia es simplemente que los datos de los destinatarios están invertidos

_Haga clic sobre la última caja de color bajo la columna Info. ¿Cuántas pestañas se muestran con este evento? Explique._
Solo 2, porque el cliente ya ha recibido la respuesta y no enviará nada más al servidor, es decir, se terminó la comunicación por lo que existe la información de entrada

_¿Qué tipos de eventos adicionales se muestran?_
UDP, TCP, STP,TFTP,USB,VTP,FTP,HTTP,HTTPS,NTP,DTP,POP3, etc etc

_¿Qué información se indica en el campo NAME :en la sección de DNS QUERY?_
www.osi.local 

_Haga clic en la ultima caja de color de Info de DNS en el event list.
Preguntas:
¿En qué dispositivo se capturó la PDU?_
En Web Client

_¿Cuál es el valor que aparece junto a ADDRESS: en la sección DNS ANSWER de Inbound PDU Details?_
IP:192.168.1.254 

_En la lista numerada directamente debajo de In Layers y Out Layers, ¿cuál es la información que se muestra en los elementos 4 y 5?_
4. The TCP connection is successful.
5. The device sets the connection state to ESTABLISHED.

_¿Cuál es el propósito de este evento, basado en la información proporcionada en el último elemento de la lista (debe ser el elemento 4)?_
Comunicar que el canal está listo para enviar más paquetes



## Ejercicio 4.7.1
_Acerque y expanda la ventana para ver todo el enrutador.
¿Qué puertos de administración están disponibles?_
Puede conectarse a la consola o al aux para administrar el dispositivo

_¿Qué interfaces LAN y WAN están disponibles en el Router este y cuántas hay?_
Dispone de GigabitEthernet 0/0 y 0/1, y serial 0/0/0 y 0/0/1


_Haga clic en la ficha CLI, presione la tecla Intro para acceder al símbolo del modo de usuario y escriba los siguientes comandos:
Abrir una ventana de configuración
Este> show ip interface brief
La salida verifica el número correcto de interfaces y su designación. La interfaz vlan1 es una interfaz virtual que sólo existe en el software.
Pregunta:
¿Cuántas interfaces físicas se enumeran?_
4

_Ingrese los siguientes comandos:
Este> show interface gigabitethernet 0/0
Pregunta:
¿Cuál es el ancho de banda predeterminado de esta interfaz?_
Full duplex 100mb/s

_Este> show interface serial 0/0/0
Pregunta:
¿Cuál es el ancho de banda predeterminado de esta interfaz?_
BW 1544 Kbit


_Paso 2: Identifique los módulos de expansión de módulos.
Preguntas:
¿Cuántas ranuras de expansión están disponibles para agregar más módulos al router East?
Una
Haga clic en Switch2. ¿ Cuántas ranuras de expansión están disponibles?_
Una

_Haga clic en Este y, a continuación, haga clic en la ficha Physical (Capa física) A la izquierda, debajo de la etiqueta Módulos, verá las opciones disponibles para expandir las capacidades del enrutador. Haga clic en cada módulo. En la parte inferior, se muestra una imagen y una descripción . Familiarícese con estas opciones._
Preguntas:
- You need to connect PCs 1, 2, and 3 to the East router, but you do not have the necessary funds to purchase a new switch. Which module can you use to connect the three PCs to the East router?
HWIC-4ESW añadirá 4 conexiones ethernet rj45
- How many hosts can you connect to the router using this module?
Uno más

_Haga clic en Switch2.
Pregunta:
¿Qué módulo se puede insertar para proporcionar una conexión óptica Gigabit al Switch3?_
PT-SWITCH-NM-1FGE

_Paso 2: Agregue los módulos correctos y dispositivos de encendido.
a.     Haga clic en Este e intente insertar el módulo adecuado del paso 1a. Los módulos se agregan haciendo clic en el módulo y arrastrándolo a la ranura vacía del dispositivo.
No se puede agregar un módulo cuando se muestra el mensaje de encendido. Las interfaces para este modelo de router no son intercambiables en caliente. El dispositivo debe estar apagado antes de agregar o quitar módulos. Haga clic en el interruptor de encendido ubicado a la derecha del logotipo de Cisco para apagar el Este. Inserte el módulo adecuado del paso 1a. Cuando haya terminado, haga clic en el interruptor de alimentación para encender el router Este.
Nota: si inserta el módulo incorrecto y necesita quitarlo, arrastre el módulo hasta su imagen en la esquina inferior derecha y suelte el botón del mouse.
b.     Con el mismo procedimiento, inserte el módulo que identificó en el Paso 1b en la ranura vacía más a la derecha en Switch2.
c.     Use el comando show ip interface brief en Switch2 para identificar la ranura en la que se colocó el módulo.
Pregunta:
¿En qué ranura se insertó?_
En la ranura 9



## Preguntas de desafío

El servidor web está "mirando" el Puerto 80
Para las solicitudes DNS el servidor está buscando el puerto 53
