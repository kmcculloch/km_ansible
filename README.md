# km_ansible

Ansible provisioning scripts to install km_bash and myvim.

## Setup

Create an `inventory.yml` file like the following:

```
---
all:
  children:
    single_user:
      hosts:
        hp18lin:
          ansible_host: hp18lin
          km_bash_prompt_name: kevin@hp18lin
          km_bash_prompt_color: Red
          km_bash_email: p.kevin.mcculloch@gmail.com
```

## Provisioning

```
ansible-playbook -i inventory.yml playbook.yml
```
