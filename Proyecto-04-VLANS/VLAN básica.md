## Proyecto 04 - Creación y concepto de VLAN simple

# Objetivo 
Demostración visual y escríta de una topología con redes locales virtuales. 

# Topología
<img width="1024" height="704" alt="image" src="https://github.com/user-attachments/assets/372c6eed-d009-4ed9-832e-d20c3e08014e" />
En primer lugar, se encuentra diseñada la topología de la red. Cada color, representa una VLAN y un departamento de una empresa, además de poseer una subred cada una. En este caso, se visualizan tres switches, dos de ellos tienen conexiones UTP de las computadoras y el que sobra, se encuentra en modo trunk, el cuál permite la comunicación entre switches. 

# Configuración de red
<img width="1822" height="656" alt="image" src="https://github.com/user-attachments/assets/ee4e3c59-6f8c-4c48-a421-909aac616d04" />
Establecí la configuración de red para cada dispositivo. Cabe destacar que, al tener subredes distintas cada VLAN tiene su propio gateway, IP y comparten máscara.

# Creación de VLAN
<img width="1375" height="698" alt="image" src="https://github.com/user-attachments/assets/0a10d193-6208-464b-9bce-c312871c6ece" />
En esta imagen, avancé con el establecimiento de las redes virtuales en el switch para que el conmutador sepa que redes debe comunicar. En la siguiente imágen, realizo la configuración de las interfaces para que puedan enviar el tráfico hacia su destino.

<img width="1365" height="691" alt="image" src="https://github.com/user-attachments/assets/b742b2fd-eafd-4f5c-b80e-cd3de00a6b9b" />
En esta captura, se puede ver como ingresé al CLI del switch y configuré las interfaces conectadas a cada dispositivo para asignar el modo "acceso" a la VLAN que corresponde. También a cada switch le asigné el modo troncal para cada interfaz conectada hacia el tercer switch que funciona como puente de comunicación. (Switch 3)

# Switch Trunk Mode (Modo troncal)
<img width="1427" height="680" alt="image" src="https://github.com/user-attachments/assets/5e0e6cda-0edd-4431-b882-98d8839c2d07" />
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
