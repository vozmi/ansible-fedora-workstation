# ansible-fedora-workstation

This repository is created to automate the process of configuring Fedora workstation using Ansible playbook.

---

## Requirements
To run this playbook you need to have `ansible` installed. You can do it with `pip` (package installer for Python).
```bash
python3 -m pip install --user ansible
```
Or you can look at [ansible installation docs](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).


To run this playbook you have to install roles for docker and java configuration. You can do it with `ansible-galaxy` command:

`ansible-galaxy install -r requirements.yml`

## Configuration

You can also configure what you want to install with variables in `vars/default_vars.ansible.yml`

```yml
---
install_java: true
install_docker: true
install_lt2p_vpn_module: true
install_telegram: true
install_vscode: true
install_edge: true
install_postman: true
install_discord: true
```

## Running the installation process

To run the playbook use `ansible-playbook` command

```bash
ansible-playbook playbook.yml -i inventory.ini -K
```