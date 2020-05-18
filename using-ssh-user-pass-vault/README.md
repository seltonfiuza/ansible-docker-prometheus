## Create a Vault file

Creating ansible-vault file for store encrypt var (ssh password and root password)

> ansible-vault create passwd.yml

Set the password for vault and the tool will start whatever editor you have defined with $EDITOR

    my_cluser_sudo_pass: osboxes.org
    ssh_pass: osboxes.org

## Run

> ansible-playbook -i hosts --ask-vault-pass --extra-vars '@passwd.yml' main.yml

And type the password for vault

### Credits
https://www.cyberciti.biz/faq/how-to-set-and-use-sudo-password-for-ansible-vault/