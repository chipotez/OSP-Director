# Laboratorio 1 
## Preparando Undercloud.
1.- Log in en nuestro laboratorio.

Para el laboratorio que estamos realizando nos conectarnos al equipo Undercloud con las siguientes credenciales:
    
    User      : mi-user
    Password  : mi-password

2.- Creación de alias de red para VLAN's.

Para crear una VLAN, se crea un alias de red sobre una interfaz de red que se conoce como la interfaz principal. La 
interfaz VLAN etiqueta los paquetes con el ID de VLAN a medida que pasan a través de la interfaz, y los paquetes de 
regreso no son etiquetados. La interfaz VLAN se puede configurar de forma similar a cualquier otra interfaz. La interfaz
principal se puede crear una interfaz de tagging VLAN 802.1Q en modo bridge, bonding o team.

1. -Cree interfaces de alias para sus VLAN utilizando la siguiente información:

  * Todas las interfaces deben ser alias para eth0.
  * La siguiente tabla proporciona los detalles adicionales necesarios para crear las interfaces:

        Nombre de la Red.   | Datos de la Red.
        -----------------   | ----------------
        External Network    | VLAN ID: 100
                            | Network: 10.1.1.0/24
                            | IP Address: 10.1.1.1
        Internal API Network| VLAN ID: 201
                            | Network: 172.16.0.1/24
                            | IP Address: 172.16.0.1
        Tenant Network      | VLAN ID: 202
                            | Network: 172.17.0.1/24
                            | IP Address: 172.17.0.1
        Storage Network     | VLAN ID: 203
                            | Network: 172.18.0.1/24
                            | IP Address: 172.18.0.1
        Storage Management Network | VLAN ID: 204
                            | Network: 172.19.0.1/24      
                            | IP Address: 172.19.0.1
        Management Network  | VLAN ID: 205
                            | Network: 172.20.0.1/24
                            | IP Address: 172.20.0.1
                    
2. -Una vez que haya terminado, reinicie el servicio de red dentro del undercloud para que los cambios surtan efecto.


