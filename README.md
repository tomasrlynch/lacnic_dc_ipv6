# Laboratorios LACNIC
Para estos cursos, los laboratorios son generados automáticamente utilizando [netlab](https://netlab.tools/). Cada uno de los directorios de los laboratorios tiene un archivo `topology.yml` y configuraciones de soporte con extensión `.j2` que son utilizados por netlab para crear cada una de las topologías con las que trabajamos.
> [!NOTE]
> Las configuraciones de los hosts no se muestran debido a que hay muchas maneras distintas de configurarlos y en este curso son simples servidores Linux. En los laboratorios utilizaremos Alpine Linux ya que viene por defecto en netlab.

## IPv6 en Data Centers
El curso "IPv6 en Data Centers" cuenta con cuatro laboratorios. Cada uno de ellos está descripto a continuación. Dentro del directorio `configuraciones` existen subdirectorios para cada uno de los labs con las configuraciones de los equipos de red.

### Laboratorio Básico
En este laboratorio se muestran las configuraciones básicas de una topología Spine y Leaf. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `labbasico`
### Laboratorio Vecinos Dinamicos BGP
En este laboratorio se muestran las configuraciones de los spines para usar vecinos dinamicos. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `vecinos_dinamicos`
### Laboratorio BGP sin Numerar
En este laboratorio se muestran las configuraciones de los spines y leaves para BGP unnumbered. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `sin_numerar`
### Laboratorio Acceso a Internet
El laboratorio muestra las distintas políticas de BGP a aplicar a los Spines y Leafs. Los componentes son:
- Dos routers de proveedores
- Dos routers de Borde
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

En el directorio `./configuraciones` encontrarán las configuraciones para el laboratorio:
1. `./configuraciones/internet_sin_filtro` este directorio contiene las configuraciones iniciales de los equipos
2. `./configuraciones/internet_con_filtro` este directorio contiene las configuraciones finales de los equipos 

Templates netlab: 
- En `acceso_internet` encontrarán los templates para generar el laboratorio sin filtros.
- En `acceso_internet_con_filtros` encontrarán los templates para generar el laboratorio con filtros.

## Servicios Avanzados de Data Center 
El curso de Servicios Avanzados cuenta con seis laboratorios. El primero es de BGP para clientes y los restantes están basados en VXLAN y EVPN.

### Servicio de BGP
El laboratorio muestra las configuraciones necesarias en los Leaves y Hosts para dar un servicio de BGP a los clientes. Los componentes son:
- Dos routers de proveedores
- Dos routers de Borde
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Con esta base se arman dos laboratorios muy parecidos pero que difieren en la configuración de los Hosts:
1. Servicio Básico de BGP en `./configuraciones/servicio_bgp_simple`
2. Servicio Anycast de BGP en `./configuraciones/servicio_bgp_anycast`

Templates netlab:
- En `servicio_bgp_simple` encontrarán los templates para generar el laboratorio sin filtros.
- En `servicio_bgp_anycast` encontrarán los templates para generar el laboratorio con filtros.

*Nota: en `./local_as` podrán encontrar un laboratorio dedicado a local AS.*

### Servicio de Redes Privadas Capa 2
El laboratorio muestra las configuraciones de VXLAN y EVPN para túneles de capa 2. Existen dos VXLAN distintas y estos son sus componentes:
- Cuatro hosts de VXLAN 101000 denominados `host[1-4]1`
- Cuatro hosts de VXLAN 101001 denominados `host[1-4]2`
- Dos hosts `host[AB]` que son clientes unicast IPv6
- Dos Spines
- Cuatro Leaves

Los archivos de configuración de este laboratorio se encuentran en `./configuraciones/vxlan_l2`

Templates netlab:
- En `vxlan_l2` encontrarán los templates para generar el laboratorio.

### Servicio de Redes Privadas Capa 3
El laboratorio muestra las configuraciones de VXLAN y EVPN para túneles de capa 3. Existen dos VXLAN distintas y estos son sus componentes:
- Cuatro hosts de VXLAN 10001 / VRF Azul denominados `host[1-4]1`
- Cuatro hosts de VXLAN 20002 / VRF Verde denominados `host[1-4]2`
- Dos hosts `host[AB]` que son clientes unicast IPv6
- Dos Spines
- Cuatro Leaves

Los archivos de configuración de este laboratorio se encuentran en `./configuraciones/vxlan_l3`

Templates netlab:
- En `vxlan_l3` encontrarán los templates para generar el laboratorio.

### Servicio de Conexión Externa
En este laboratorio se extiende el concepto de VXLAN capa 2 para dar servicios de conectividad externa. Para simplificar el laboratior solamente hay una VXLAN y los siguientes componentes:
- Un spine
- Dos leaves, uno dedicado a conectividad externa
- Un host conectado a la red de data center
- Un router y un host simulando una red remota en la oficina del cliente.

Los archivos de configuración de este laboratorio se encuentran en `./configuraciones/conexion_externa`

Templates netlab:
- En `conexion_externa` encontrarán los templates para generar el laboratorio.`
### Interconexión de Data Centers (DCI)
El laboratorio de DCI simula dos data centers interconectados por sus routers de borde. Cada DC cuenta con:
- Un router de borde
- Dos spines
- Dos leaves
- Dos hosts

Los archivos de configuración de este laboratorio se encuentran en `./configuraciones/dci`

Templates netlab:
- En `dci` encontrarán los templates para generar el laboratorio.
### Interconexión de Data Centers (DCI) para Múltiples Data Centers
El laboratorio de DCI simula tres data centers interconectados por sus routers de borde. Cada DC cuenta con:
- Un router de borde
- Un spine
- Un leaf
- Un host

Los archivos de configuración de este laboratorio se encuentran en `./configuraciones/dci_rs`

Templates netlab:
- En `dci_rs` encontrarán los templates para generar el laboratorio.
