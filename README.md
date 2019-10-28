# Dev-Fine 

ansible role which defines and installs my development environment.


Includes the following:
* [koichirok/ansible-role-google-chrome][1] - Google Chrome
* [geerlingguy/ansible-role-docker][2] - Docker & Docker Compose
* [chrgue/ansible-role-dev-essentials][3] - Command line tools
* [viasite-ansible/ansible-role-zsh][4] - Full zsh installation


## Quick Start

Without much knowledge about ansible you can just copy & paste the following command in your terminal and you are good to go:

    $ bash <(wget -qO- https://raw.githubusercontent.com/chrgue/dev-fine/master/install.sh)

## Manual - ansible way

#### Preconditions

First make sure you have ansible installed

    $ sudo apt-add-repository -y ppa:ansible/ansible
    $ sudo apt update
    $ sudo apt install -y ansible


#### Download ansible role

    $ ansible-galaxy install chrgue.dev_fine


#### Playbook usage:

    # playbook.yml
    - name: Setup full development enviroment
      hosts: localhost
      connection: local
      roles:
        - role: chr.dev_fine
          
#### Run playbook

    $ ansible-playbook playbook.yml



Preparation:

    $ sudo apt install ansible
    $ cd <project_dir>
    # install required ansible roles 
    $ ansible-galaxy install -r requirements.yml



## Quick Start

Without much knowledge about ansible you can just copy & paste the following command in your terminal and you are good to go:

    $ bash <(wget -qO- https://raw.githubusercontent.com/chrgue/dev-fine/master/install.sh)



Full environment:

    $ cd <project_dir>
    $ ansible-playbook playbooks/full.yml --ask-become

Essential environment: 

    $ cd <project_dir>
    $ ansible-playbook playbooks/essentials.yml --ask-become

Java environment:

    $ cd <project_dir>
    $ ansible-playbook playbooks/java.yml --ask-become
    
    
[1]: https://github.com/koichirok/ansible-role-google-chrome
[2]: https://github.com/geerlingguy/ansible-role-docker
[3]: https://github.com/chrgue/ansible-role-dev-essentials
[4]: https://github.com/viasite-ansible/ansible-role-zsh