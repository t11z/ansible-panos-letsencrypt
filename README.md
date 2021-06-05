# ansible-panos-letsencrypt
Ansible playbook to automatically create SSL certificates via Let's Encrypt and push them to Palo Alto Networks NGFWs

## Features
This playbook features the DNS-01 ACME challenge type. There are currently two options to deploy the ACME challenge:
* dynamic updates for BIND DNS server (nsupdate)
* GoDaddy API

You need to acquire the necessary secret keys for the corresponding DNS provider first.

## Requirements
  ```Bash
  pip install pan-python cryptography requests requests-toolbelt pyOpenSSL
  ```