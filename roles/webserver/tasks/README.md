webserver
===============

This role contains httpd webserver role that will install httpd, update the html, and run httpd service. Lastly, it will create Route53 record.

Requirements
------------

This role is expecting to be run on a Red Hat based system.  E.g. CentOS or Amazon Linux

Role Variables
--------------

url - url of a custom html page to replace the default index.html.
ip - the public IP address of the EC2 instance.

Dependencies
------------

None

Example Playbook
----------------

Just apply the role:

    - hosts: servers
      roles:
         - role: webserver
           url: https://path/to/custom/index.html
           ip:  "{{ item.public_ip }}"

License
-------

Commercial

Author Information
------------------

Antonio
