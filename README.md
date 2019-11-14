# Ansible Playbook with setup web server using WordOps as basis. 

More information about EasyEngine can be found at https://wordops.net/

OS requirements Ubuntu 14+

# Followig ansible variables can/should be used during executing
aws_access_key_id - AWS access key for backup user \
aws_secret_access_key - AWS secret key for backup user \
wo_name - Name which will be used during WO setup \
wo_email - email address which will be used for WO setup and Let's Encrypt

# Example of executing
```
Server setup:
ansible-playbook  -i <IP_OF_SERVER>, -u root wo-ansible.yaml --extra-vars "aws_access_key_id=XXXXXXXXXXXX aws_secret_access_key=YYYYYYYYYYYYYYY wo_name=Test wo_email=ansible@ansible.com ansible_python_interpreter=/usr/bin/python3"

Mysql setup:
ansible-playbook  -i <IP_OF_SERVER>, -u root wo-mysql-ansible.yaml --extra-vars "aws_access_key_id=XXXXXXXXXXXX aws_secret_access_key=YYYYYYYYYYYYYYY wo_name=Test wo_email=ansible@ansible.com ansible_python_interpreter=/usr/bin/python3"

Postfix setup:
ansible-playbook  -i <IP_OF_SERVER>, -u root postfix-setup.yaml --extra-vars "hostname=XXXXXXXXXX.com ansible_python_interpreter=/usr/bin/python3"
```
