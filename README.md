# ansible-initial-deploy
An ansible playbook to run some common and initial server setup commands.  Designed for Ubuntu 16.04 on DigitalOcean, Linide, etc.

# What the script does
- apt-get update && upgrade
- sets a hostname
- sets timezone to UTC
- installs NTP
- allows OpenSSH in UFW and enables UFW

# How to use the script
- have ansible installed
- have an inventory file
- if running only this script, run it on one server at a time, alternatively conditions will need to be set for mulitple hostnames
- run the script, ansible-playbook initial-server-setup.yml --extra-vars "hosename=hostname

