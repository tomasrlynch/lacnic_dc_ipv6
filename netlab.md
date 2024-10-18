# Instalación
1) sudo apt-get update && sudo apt-get install -y python3-pip
2) sudo python3 -m pip install networklab
3) netlab install ubuntu ansible libvirt containerlab #(decir que si a todo)

Si reciben un error parecido a este,
packaging.version.InvalidVersion: Invalid version: 'xxxxxxxxxx'

sigan las siguientes instrucciones:
0.1) sudo snap install yq
0.2) for MODULO in  pyopenssl cryptography testresources pyyaml httplib2 jinja2 six bracket-expansion netaddr pynacl lxml paramiko netmiko ansible-pylibssh textfsm ttp jmespath ntc-templates yamllint ansible; do echo instalando $MODULO; sudo pip3 install $MODULO; done
0.3) sudo vi /usr/local/lib/python3.8/dist-packages/netsim/install/ansible.sh
Cambiar cambiar línea 32 para que quede: REPLACE=""
cambiar linea 33 para que quede: IGNORE=""
eliminar yq del final de la lunea 52
0.4) netlab install ubuntu ansible libvirt containerlab

# Uso
Copien los archivos topology.yml, o descarguen el repositorio en el servidor instalado.
Luego hagan `netlab up`
Ingresen a los equipos haciendo `netlab connect <nombre del equipo>`
El lab lo pueden dar de baja con `netlab down`
