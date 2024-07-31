vCenter Install
=========
Despliega una maquina virtual de vCenter en un servidor ESXi y agrega el servidor al vCenter

Requirements
------------
community.general de Ansible
python3-pyvmomi v6.7.4 o superior

Role Variables
--------------
- validate_certs: 'no' si no se han configurado los certificados SSL, 'yes' sino
- esxi_server: url o direccion ip del servidor ESXi
- esxi_username: usuario del servidor ESXi
- esxi_password: contraseña del servidor ESXi
- path_ova_file: ruta absoluta al archivo OVA en la maquina virutal de Ansible
- vcenter_datastore: nombre del Datastore donde se va a desplegar el vCenter
- vcenter_name: nombre de la maquina virtual del vCenter
- vcenter_network: nombre de la red de trabajo del vCenter
- vcenter_username: nombre del usuario de acceso a vSphere, tipicamente "administrator@vsphere.local"
- vcenter_password: contraseña SSO del usuario de vSphere
- vcenter_hostname: url de acceso o direccion ip del vCenter
- vcenter_address: direccion ip del vCenter
- vcenter_datacenter: nombre del datacenter que se desea crear
- vcenter_cluster: nombre del cluster que se desea crear
- net_prefix: longitud de mascara de red, en notacion CIDR, por ej. "24"
- net_gateway: direccion ip del gateway
- dns_servers: direccion ip del servidor dns, puede ser una lista separada por comas
- domain: dominio de resolucion DNS
- searchpath: igual que el "domain"
- vcsa_size: tamaño del despliegue deseado para el vCenter, opciones posibles son: tiny,small,medium,large, o infrastructure

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - vcenter_install

License
-------

BSD

Author Information
------------------

Mauro Ezequiel Schinca, mschinca@bancocredicoop.coop & Matías Gabriel Oviedo, mgoviedo@bancocredicoop.coop

