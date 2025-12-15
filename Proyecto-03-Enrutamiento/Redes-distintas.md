## Proyecto 03 - Enrutamiento de redes distintas (Sucursales)

# Objetivo
Demostración visual y explicada del enrutamiento estático entre dos redes distintas, simulando oficinas a distancia de una empresa.

# Topología
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/5fcef337-fc0d-457d-933e-14eabf1e181d" />
La topología de esta red está compuesta de dos redes con distinta IP y dos routers que se interconectan con una conexión serial. Esto permite el enrutamiento entre departamentos, oficinas, sucursales, etc. 

# Configuración de red
<img width="1919" height="934" alt="image" src="https://github.com/user-attachments/assets/e0529571-23b3-4837-adfa-483e031e4dff" />
En esta imagen, aplica más de lo mismo. Es la configuración de red pero con la diferencia de que para cada una, se asigna un host nuevo y gateway correspondiente a cada enrutador. La "Sucursal A" tiene 192.168.1.0 /24 y la "Sucursal B" dispone de 192.168.2.1 /24.

# Enrutamiento estático
<img width="1920" height="912" alt="image" src="https://github.com/user-attachments/assets/6ad0fd29-b128-4d91-89cf-36456e399f94" />
En esta imagen, se puede visualizar que la topología ahora tiene una nueva IP y esta corresponde al enlace entre ambos routers. Acá, configuré cada interfaz serial asignandole a cada router una IP 10.0.0.1 y 10.0.0.2 con máscara 255.255.255.252, correspondiente a la IP del enlace: 10.0.0.0 /30. La máscara que termina en ".252" define que hay 4 direcciones totales, una para broadcast, una para red y las otras dos para hosts, que son los enrutadores. 

<img width="1920" height="897" alt="image" src="https://github.com/user-attachments/assets/c309339c-6bf7-4438-a37f-2a6079f10e41" />
Luego apliqué la configuración para cada router, asignando las direcciones para las tablas de rutas. Mediante el CLI, apliqué la configuración correspondiente con la IP de la red a la cuál se debe comunicar, la máscara y la IP del serial por donde debe viajar las tramas. El comando utilizado es "ip route (IP de red contraria) (máscara) (IP del puerto serial contrario)".

# Prueba de conectividad
<img width="1916" height="930" alt="image" src="https://github.com/user-attachments/assets/5b8048ed-1fe1-4287-a75c-adba99640d4f" />
<img width="1917" height="944" alt="image" src="https://github.com/user-attachments/assets/94f6b390-4330-4e1f-8d62-8e97db8afa81" />
<img width="1920" height="932" alt="image" src="https://github.com/user-attachments/assets/6ee8eee3-bc09-448f-b6f0-be685f54099b" />
<img width="1913" height="943" alt="image" src="https://github.com/user-attachments/assets/96ed611d-da6a-4738-8235-78c673f488a2" />
Finalmente, los dispositivos se pueden comunicar gracias al correcto enrutamiento. En este caso, se probaron dos equipos, la PC 3 con el DESKTOP A y la PC 5 con el DESKTOP C.

# Conceptos aplicados
- Modelo OSI - Capa 1, 2, 3 (física, enlace, red)
- Pruebas de red (ICMP)
- Routing
- Gateway
- Switching 
