# Introducción
> Agradezco a Ariel Weher por haberme ayudado a encontrar cómo subsanar el error de instalación.
Esta es una guía simple para que puedan instalar netlab, bajen el repositorio y corran los laboratorios. Les recomiendo mucho ir a la [página del projecto netlab](https://netlab.tools/) y leer las instrucciones para poder armar o modificar los laboratorios a su mejor parecer.
# Requerimientos
Los siguientes no son los requerimientos mínimos del servidor, son las propiedades del servidor donde corrí sin problemas todos los laboratorios del curso.
- Ubuntu 20.04 LTS x64
- 8 x Virtual CPU
- 16 GB RAM
- 160 GB Disco
# Instalación de netlab
Los pasos que siguen los pueden ver comentados en la [página de instalación de netlab](https://netlab.tools/install/):
1) `sudo apt-get update && sudo apt-get install -y python3-pip`
2) `sudo python3 -m pip install networklab`
3) `netlab install ubuntu ansible libvirt containerlab` **decir que si a todo**
## Error en la Instalación de netlab
Si reciben un error parecido a este `packaging.version.InvalidVersion: Invalid version: 'xxxxxxxxxx'` sigan las siguientes instrucciones luego del tercer paso:
1) `sudo snap install yq`
2) ```for MODULO in  pyopenssl cryptography testresources pyyaml httplib2 jinja2 six bracket-expansion netaddr pynacl lxml paramiko netmiko ansible-pylibssh textfsm ttp jmespath ntc-templates yamllint ansible; do echo instalando $MODULO; sudo pip3 install $MODULO; done```
3) `sudo vi /usr/local/lib/python3.8/dist-packages/netsim/install/ansible.sh`
- Cambiar cambiar línea 32 para que quede: `REPLACE=""`
- Cambiar linea 33 para que quede: `IGNORE=""`
- Eliminar `yq` del final de la línea 52
4) `netlab install ubuntu ansible libvirt containerlab`
# Usando netlab
Para utilizar los laboratorios de este repositorio, simplemente bajen el mismo. Una vez bajado, cambien al directorio del lab. Para levantar el lab simplemente corran `netlab up`.

Luego, ingresen a los equipos haciendo `netlab connect <nombre del equipo>`.

Una vez finalizado con el lab, lo pueden dar de baja con `netlab down`

Nota: Si no quieren bajar el repositorio completo, busquen el archivo `topology.yml` dentro de cada directorio, cópienlo a sus máquinas y sigan las instrucciones de acceso explicadas anteriormente.
