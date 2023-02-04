arch-iac
=========

An Ansible playbook that sets up an Arch Linux laptop by installing a minimal gnome and essential tools. 

This playbook should be executed on localhost, with proper access to sudo.

Deployment
------------
- Install `ansible` and `git`

- Clone this repo

- Install the playbook dependency by running `ansible-galaxy install -r requirements.yml`

- Deploy the most suitable playbook by `ansible-playbook <playbook.yml> -K -vvvv`

Playbooks / Roles
--------------
- `deploy_standard.yml` install packages and flatpak apps
- `deploy_noflatpak.yml` doesn't install flatpak apps. 

TBD
---
add a role to install miniconda and some other stuffs, i guess
