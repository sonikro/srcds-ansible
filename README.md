# srcds-ansible
Ansible playbooks for srcds dedicated servers

These playbooks were designed and tested to run with Ubuntu Server 16.04 64bits   
# tf2_server

Setups a basic tf2 server, no extra configuration

Example usage:

```bash
ansible-playbook -i inventory.yaml "playbooks/setup-tf2-server.yml" -K
```

# tf2_server_competitive

Setups a tf2 server with competitive settings (cfg, maps, plugins)

```bash
ansible-playbook -i inventory.yaml "playbooks/setup-tf2-server-competitive.yml" -K
```

# Inventory

The inventory.yaml file is in the gitignore, so each of you can define your own inventory
You might consider using AWX or Ansible Tower to manage the inventory as well