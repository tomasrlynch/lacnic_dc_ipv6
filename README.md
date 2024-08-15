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

### Servicio de Redes Privadas
### Servicio de Conexión Externa
### Interconexión de Data Centers (DCI)
