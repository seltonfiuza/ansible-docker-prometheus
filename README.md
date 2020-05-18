# Using basic Ansible to deploy Docker Prometheus ON VMs


    .
    ├── README.md
    ├── using-ssh-pem
    │   ├── hosts
    │   ├── main.yml
    │   ├── prometheus.yml
    │   └── README.md
    ├── using-ssh-user-pass
    │   ├── hosts
    │   ├── main.yml
    │   ├── prometheus.yml
    │   └── README.md
    └── using-ssh-user-pass-vault
        ├── hosts
        ├── main.yml
        ├── passwd.yml
        ├── prometheus.yml
        └── README.md

hosts file: ansible inventory with hosts and variables
> https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html

main.yml: main file of ansible playbook. Roles was not necessary.
> https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html

prometheus.yml: prometheus file with targets.
> https://prometheus.io/docs/prometheus/latest/configuration/configuration/

The using-ssh-user-pass folder is not recommended, because the password of root user and ssh is in plain text inside of the inventory file, ansible-vault is recommended.

> https://docs.ansible.com/ansible/latest/user_guide/vault.html