# Dev-Fine 

Defines and installs my development environment with ansible.



To run the full installation:
```bash
# install ansible
$ sudo apt install ansible
$ cd <project_dir>
# install required ansible roles 
$ ansible-galaxy install -r requirements.yml
$ ansible-playbook ./install.yml
```

To choose certain aspects of the setup you can do that by tags.
For example to install a chrome browser, common tooling and docker run the following command:
```bash
# install ansible
$ sudo apt install ansible
$ cd <project_dir>
# install required ansible roles 
$ ansible-galaxy install -r requirements.yml
$ ansible-playbook ./install.yml --tags chrome,tools,docker
```

Supported tags:

| tag | features   |
|---|---|
| chrome  | <ul><li>installs chrome browser</li></ul> |
| docker  | <ul><li>installs docker community edition</li><li>puts current user into docker group</li></ul> |
| java | <ul><li>installs JDK</li><li>installs java tools (e.g. maven)</li><li>installs intellj community edition</li></ul> |
| tools | <ul><li>installs common commandline tools</li></ul> |
| zsh | <ul><li>installs zsh</li></ul> |

