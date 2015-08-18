*****
NGINX
*****

Instalación de [nginx](http://nginx.org/).

**********
Requisitos
**********

Sistemas operativos soportados:

- CentOS 7 

*********
Variables
*********

Sólo si se va a utilizar como reverse proxy de `kibana`_::

	---
	# defaults file for nginx
	# KIBANA
	kibana_nginx: true # Verdadero si se usa nginx como reverse proxy para kibana (por defecto false)
	kibana_url: web_url # URL para acceder a la web de kibana (nginx reverse proxy)
	kibana_port: 5601 # Puerto de escucha de kibana
	kibana_web_user: web_user # Usuario con acceso a la web de kibana
	kibana_web_password: web_password # Contraseña para el usuario con acceso a la web de kibana

************
Dependencias
************

Ninguna.

*******************
Ejemplo de playbook
*******************

    - hosts: servers
      roles:
         - { role: alkher.nginx }

********
Licencia
********

BSD

*****
Autor
*****

Andoni Alcalde
- @alkher
- http://zenway.es
- alcher [at] zenway [dot] es

.. _nginx: http://nginx.org/
.. _kibana: https://www.elastic.co/products/kibana