## Proyecto 04 - Creación y concepto de VLAN simple

# Objetivo 
Demostración visual y escríta de una topología con redes locales virtuales. 

# Topología
<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/ed2520e6-3541-4c5c-962c-9dd44b7388f0" />
En primer lugar, se encuentra diseñada la topología de la red. Cada color, representa una VLAN y un departamento de una empresa, además de poseer una subred cada una. En este caso, se visualizan tres switches, dos de ellos tienen conexiones UTP de las computadoras y el que sobra, se encuentra en modo trunk, el cuál permite la comunicación entre switches. 

# Configuración de red
<img width="1810" height="684" alt="image" src="https://github.com/user-attachments/assets/5717ca27-54e6-48db-836e-3be9f0f3ec92" />
Establecí la configuración de red para cada dispositivo. Cabe destacar que, al tener subredes distintas cada VLAN tiene su propio gateway, IP y comparten máscara.

# Creación de VLAN
<img width="1397" height="655" alt="image" src="https://github.com/user-attachments/assets/b92d83ae-9d95-4ed1-b246-f9c7c014504f" />
En esta imagen, avancé con el establecimiento de las redes virtuales en el switch para que el conmutador sepa que redes debe comunicar. En la siguiente imágen, realizo la configuración de las interfaces para que puedan enviar el tráfico hacia su destino.

<img width="1307" height="668" alt="image" src="https://github.com/user-attachments/assets/0b2f7ddf-789b-4efb-b69e-1a1364f86d3c" />
En esta captura, se puede ver como ingresé al CLI del switch y configuré las interfaces conectadas a cada dispositivo para asignar el modo "acceso" a la VLAN que corresponde. También a cada switch le asigné el modo troncal para cada interfaz conectada hacia el tercer switch que funciona como puente de comunicación. (Switch 3)

# Switch Trunk Mode (Modo troncal)
<img width="1401" height="685" alt="image" src="https://github.com/user-attachments/assets/806049f9-0ad8-4ae6-993a-6cf266efc4d3" />
Finalmente apliqué la configuración del tercer switch como "modo troncal" y habilité el tráfico de las VLAN 10 y 20 para las interfaces FastEthernet0/1 y 0/2. Gracias a esta serie de configuraciones, el tráfico funciona correctamente entre los dispositivos y segmenta las subredes en redes virtuales.

# Prueba de conectividad
<img width="1075" height="854" alt="image" src="https://github.com/user-attachments/assets/c1af0021-270f-41ad-9638-10aef965632e" />
<img width="1095" height="878" alt="image" src="https://github.com/user-attachments/assets/b79264d7-b334-44d3-b26c-83e233bd2621" />
Acá se visualiza como existe una correcta comunicación entre redes virtuales.

<img width="1027" height="873" alt="image" src="https://github.com/user-attachments/assets/eb80da58-5bc2-4e4b-9645-6b90bcc8a1a2" />
Acá se visualiza que la trama violeta, no puede llegar a la red virtual contraria, por lo que demuestra una correcta segmentación.

# Final
Con este ejemplo quiero demostrar que puedo comprender como funciona la segmentación de red y como las tramas viajan a través de las rutas hacia su destino. Próximamente, estaré subiendo proyectos de enrutamiento dinámico y otras topologías. 

# Conceptos aplicados
- Modelo OSI - Capa de enlace, segmentación, tramas, cables de cobre, cruzado. 
- Pruebas de red (ICMP)
- Switching (Conmutación)
