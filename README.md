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

# Download maps from FastDL

If you have a FastDL endpoint hosted in AWS S3, you can pass the following variables:
- aws_secret_access_key
- aws_access_key_id
- aws_storage_bucket_name

And the automation will list all the files in tf/maps, download and extract then to your servers tf/maps, so your server is always in sync with your FastDL server

# Infrastructure Tips

Usually 4GB of Ram and 2 cores is more than enough to hold on a server with 24+ players


# Inventory

The inventory.yaml file is in the gitignore, so each of you can define your own inventory
You might consider using AWX or Ansible Tower to manage the inventory as well