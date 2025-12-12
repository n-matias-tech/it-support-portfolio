# Proyecto 01 – Comunicación LAN con Router (Capa 2)

## Objetivo
Demostrar la comunicación en una red LAN, el funcionamiento de la conmutación en Capa 2 y el rol del router como puerta de enlace.

## Topología
<img width="1065" height="702" alt="Red LAN" src="https://github.com/user-attachments/assets/b423ebc4-be45-45fd-9378-0d5b6e1cd799" />
En la imagen se puede visualizar la topología de una red LAN. Asigné la IP de red, el rango de Host, el broadcast y el gateway.

## Configuración de red
<img width="1339" height="712" alt="Red LAN 2" src="https://github.com/user-attachments/assets/a6040e5f-e88d-491b-a598-e10750f1fb5e" />
En este ejemplo se utilizó configuración IPv4 manual con fines demostrativos, para evidenciar el entendimiento del direccionamiento y los parámetros de red. (Ignorar IPv6, no es relevante)
En un entorno laboral, lo recomendado es el uso de DHCP para minimizar errores de configuración.

## Prueba de conectividad
<img width="1590" height="851" alt="Red LAN 3" src="https://github.com/user-attachments/assets/f851d760-0fc4-4620-b9a4-2c1149d067ee" />
Finalmente, utilicé este ejemplo para demostrar como se estableció la comunicación correctamente, el router cuenta con su interfaz configurada como puerta de enlace de la red.
Se puede visualizar la trama ICMP (diagnóstico de red) viajando por las conexiones hasta el router desde la PC de RRHH.

## Conceptos aplicados
- Modelo OSI - Capa 2
- Pruebas de red (ICMP)
- Gateway
