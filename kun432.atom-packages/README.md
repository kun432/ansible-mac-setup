atom-packages
=============

Ansible role for installing pacakges for the Atom editor

Forked from [hnakamur/ansible-role-atom-packages](https://github.com/hnakamur/ansible-role-atom-packages) and just remove tasks/main.yml, because I prefer to use "apm" as a module to as a role.

I'm not sure if this is a right way, please PR.

Example Playbook
-------------------------

    - hosts: localhost
      connection: local
      gather_facts: no           
      sudo: no
      vars:
        atom_packages:
          - project-manager
          - recent-files
      tasks:
        - name: add atom packages
          apm: name={{ item }} state=latest
          with_items: "{{ atom_packages }}"
          when: atom_packages
      roles:
        - hnakamur.atom-packages
