# Dev-Fine 

Defines and installs my development environment with ansible.



Preparation:

    $ sudo apt install ansible
    $ cd <project_dir>
    # install required ansible roles 
    $ ansible-galaxy install -r requirements.yml


Full environment:

    $ cd <project_dir>
    $ ansible-playbook playbooks/full.yml --ask-become

Essential environment: 

    $ cd <project_dir>
    $ ansible-playbook playbooks/essentials.yml --ask-become

Java environment:

    $ cd <project_dir>
    $ ansible-playbook playbooks/java.yml --ask-become