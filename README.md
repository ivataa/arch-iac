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
> !! WARNING: NEVER EXECUTE THE PLAYBOOK AS ROOT !!
### `deploy_standard.yml` 
In short, this playbook:
- Sets up gdm
- Installs bloatless GNOME
- Sets up CUPS
- Sets up yay (Yet another Yogurt)
- Installs [tools](roles/arch_basics/vars/main.yml), e.g tldr, fish, htop, nvim
- Installs and sets up Miniconda3
And sets up Flatpaks:
- Install [apps](roles/flatpak/vars/main.yml)
- Customize them (only librewolf for now)

### `deploy_noflatpak.yml` 
Same as `deploy_standard.yml` but it won't do the flatpak stuffs.

TBD
---
add a role to install miniconda and some other stuffs, i guess
