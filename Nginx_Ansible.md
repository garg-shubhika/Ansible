### Install Ansible
`` bash
sudo apt update
sudo apt install ansible -y
``

### Install NGINX
`` bash
sudo apt install nginx -y
``

### Write install_nginx_wsl.yml

`` bash
nano install_nginx_wsl.yml
``

### Run the Playbook
`` bash
ansible-playbook install_nginx_wsl.yml
``

### Starting NGINX After Reboot
`` bash
sudo bash /etc/init.d/nginx_autostart
``

### Find WSL's IP Address
`` bash
ip addr show eth0 | grep 'inet ' | awk '{print $2}' | cut -d'/' -f1
``

### Access NGINX in Your Browser, Example:
`` bash
http://172.30.240.1
``
