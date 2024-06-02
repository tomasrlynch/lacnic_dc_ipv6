# Laboratorios LACNIC
El curso "IPv6 en Data Centers" cuenta con cuatro laboratorios. Cada uno de ellos está descripto a continuación. Dentro del directorio `configuraciones` existen subdirectorios para cada uno de los labs con las configuraciones de los equipos de red.

Para este curso, los laboratorios son generados automáticamente utilizando [netlab](https://netlab.tools/). Cada uno de los directorios de los laboratorios tienen un archivo `topology.yml` y configuraciones de soporte con extensión `.j2` que son utilizados por netlab para crear cada una de las topologías con las que trabajamos.
> [!NOTE]
> Las configuraciones de los hosts no se muestran debido a que hay muchas maneras distintas de configurarlos. En los laboratorios utilizaremos Alpine Linux ya que viene por defecto en netlab.
## Laboratorio Básico
En este laboratorio se muestran las configuraciones básicas de una topología Spine y Leaf. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `labbasico`
## Laboratorio Vecinos Dinamicos BGP
En este laboratorio se muestran las configuraciones de los spines para usar vecinos dinamicos. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `vecinos_dinamicos`
## Laboratorio BGP sin Numerar
En este laboratorio se muestran las configuraciones de los spines y leaves para BGP unnumbered. Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Template netlab: `sin_numerar`
## Laboratorio Acceso a Internet
El laboratorio muestra las distintas políticas de BGP a aplicar a los Spines y Leafs. Los componentes son:
- Dos routers de proveedores
- Dos routers de Edge
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

En el directorio `./configuraciones` encontrarán las configuraciones para dos laboratorios:
1. `./configuraciones/internet_sin_filtro` este directorio contiene las configuraciones iniciales de los equipos
2. `./configuraciones/internet_con_filtro` este directorio contiene las configuraciones finales de los equipos 

Template netlab: `acceso_internet`
