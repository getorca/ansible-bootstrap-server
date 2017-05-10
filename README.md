# Ansible Bootsrap Server
An ansible playbook to bootsrap a Ubuntu 16.04LTS server.  It runs some common and initial server setup commands.  Designed for Ubuntu 16.04 on DigitalOcean, Linide, etc.

# What the script does
- Fix for Ubuntu 16.04 LTS that doesn't come with certain modules required by ansible
- apt-get update && upgrade
- sets a hostname
- sets timezone to UTC
- installs NTP
- allows OpenSSH in UFW and enables UFW

# How to use the script
- have ansible installed and configured
- have an inventory file with a hostname var set for each host
- run the script, ansible-playbook bootstrap-server.yml --extra-vars "host=YOUR_HOST_OR_GROUP_FROM_INVENTORY_FILE"
