
Usage instructions
==================

Encrypted secrets
-----------------

Some variables are stored in encripted files using ansible-vault.
The vault passphrase are also encrypted using my GPG public key.

    GPG ID: 0E1A33F3
    GPG uid: Juan Menéndez Blanco <juanmb@gmail.com>

Edit `/etc/ansible/ansible.cfg` and change the line:

    vault_password_file = open_the_vault.sh


Running the playbook
--------------------

Install required roles:

    sudo ansible-galaxy install Stouts.openvpn geerlingguy.pip stefangweichinger.ansible_rclone

Run the playbook site.yml using the provided inventory file. For example:

    ansible-playbook -i hosts -l merak vst.yml
