## ansible-training

Plan for ansible-training development:
```
- new host role
    - configure user in 'sudoers' group
    - enable UFW with custom SSH port open
    - apt update and upgrade
    - apt remove unneeded packages

- wordpress
    - install/configure nginx 
    - install/configure mariadb
    - install PHP and PHP extensions
    - download and deploy Wordpress installer
    - certbot auto-deploy SSL cert
```
... more to be added.



Roles:
- users
    - create standard user in sudoers group
- reboot
    - role to reboot "{{ custom_host }}"
- ping
    - role to ping "{{ custom_host }}"
- ufw
    - enable firewall and allow custom SSH port
- pkgs
    - base packages to install on all hosts
- certbot
    - automatically generate LetsEncrypt certificate with certbot
- zabbix_agent2
    - deploy preconfigured zabbix-agent2 to a host
- zabbix_server
    - deploy Zabbix Server to host (Frontend, Engine, Database)
- wordpress
    - deploy Wordpress with Nginx, PHP and Extensions, and MariaDB 
