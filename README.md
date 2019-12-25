# srcds-ansible
Ansible playbooks for srcds dedicated servers

# tf2_server
This playbook was designed to run with Ubuntu Server 16.04 64bits   

Example usage:

```bash
ansible-playbook -i inventory.yaml "/home/sonikro/sources/open-source/sonikro/srcds-ansible/playbooks/setup-tf2-server.yml" -K
```