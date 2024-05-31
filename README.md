# Laboratorios LACNIC
El curso "IPv6 en Data Centers" cuenta con cuatro laboratorios. Cada uno de ellos está descripto a continuación.
Dentro del directorio "configuraciones" existen subdirectorios para cada uno de los labs con las configuraciones de los equipos de red.

Para este curso, los laboratorios son generados automáticamente utilizando [netlab](https://netlab.tools/). Cada uno de los directorios de los laboratorios tienen un archivo `topology.yml` que es utilizado por netlab para crear cada una de las topologías con las que trabajamos.
> [!NOTE]
> Las configuraciones de los hosts no se muestran debido a que hay muchas maneras distintas de configurarlos. En los laboratorios utilizaremos Alpine Linux ya que viene por defecto en netlab.
## Laboratorio Básico
Directorio: `labbasico`

En este laboratorio se muestran las configuraciones básicas de una topología Spine y Leaf.
Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts
## Laboratorio Vecinos Dinamicos BGP
Directorio: `vecinos_dinamicos`

En este laboratorio se muestran las configuraciones de los spines para usar vecinos dinamicos
Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts
## Laboratorio BGP sin Numerar
Direcotrio: `sin_numerar`

En este laboratorio se muestran las configuraciones de los spines y leaves para BGP unnumbered
Los componentes son:
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts
## Laboratorio Acceso a Internet
Directorio: `acceso_internet`

El laboratorio muestra las distintas políticas de BGP a aplicar a los Spines y Leafs.
Los componentes son:
- Dos routers de proveedores
- Dos routers de Edge
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts
