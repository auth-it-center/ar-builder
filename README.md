ar-builder
==========

Ansible playbook used to build and release ar mini project related packages. 

To use 

1. edit the inventory to match the hostname of the machine you intend to use for building the packages, and 
2. modify the `group_vars/ar-builbers` file so that it contains the updated list of packages you wish to import via Koji on the repository. 

Then command to use afterwards is:

`ansible-playbook -v builder.yml -i inventory --extra-vars="koji_tag=centos6-arstats-devel synnefo_token=MySynnefoToken"`
