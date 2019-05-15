# Dev-Fine 

Defines and installs my development environment with ansible.


### Java
* Installs Zulu JDK **(todo)**
* Installs Intellj Community Edition
* Installs common java tools (e.g. maven)

### python
* Installs PyCharm Community Edition **(todo)**
* Install virtual env wrapper **(todo)**
* Install common python packages (scikit-learn etc.) **(todo)**

### Docker
 - Installs docker community edition
 - Installs docker-compose
 - Adds current user to docker group (to perform docker without sudo)
 - Downloads common images (missing)

### Database Tooling
 - Robo T3 for mongodb **(todo)**
    
### Common
 - Installs git 
 - Configures git
   - Sets aliases
   - Set git config for different git project (missing)
 - Installs Google Chrome Browser
 - Installs zsh with
 - Installs Printer Driver **(todo)**
 - Installs common util packages (curl, wget etc.)


HowTo:
```bash
$ sudo apt install ansible
$ cd <project_dir>
$ ansible-playbook -i ./hosts ./install.yml
```

