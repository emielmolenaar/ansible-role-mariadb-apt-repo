MariaDB APT repository role for Ansible
=================

A simple role for adding the [MariaDB APT repository](https://downloads.mariadb.org/mariadb/repositories/) on your APT-enabled hosts using [Ansible](http://www.ansibleworks.com/).

Usage
-----

This role uses [APT](https://docs.ansible.com/ansible/latest/modules/apt_module.html) to ensure the repository is added on your hosts. You might checkout Jeff Geerling's [MySQL Role](https://github.com/geerlingguy/ansible-role-mysql) for actually installing and configuring MariaDB on your hosts.

Clone this repo into your roles directory:

    $ git clone https://github.com/emielmolenaar/ansible-role-mariadb-apt-repo.git roles/mariadb-apt-repo

And add it to your play's roles:

    - hosts: ...
      roles:
        - mariadb-apt-repo
        - ...

I recommend using a `requirements.yml` in your roles directory though:

    - src: https://github.com/emielmolenaar/ansible-role-mariadb-apt-repo.git
      name: mariadb-apt-repo

Installing the role will require a `ansible-galaxy install -r ./roles/requirements.yml -p ./roles` from the root directory of your playbook.
