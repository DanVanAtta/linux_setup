## Run setup:

```
ssh-keygen -t ed25519
 # Add SSH key to github.com
sudo apt install -y git
mkdir ~/work/
cd ~/work/
git clone git@github.com:DanVanAtta/linux_setup.git
cd linux_setup/
./run-setup
```


## Install List

The following are installed/configured:
 
- Grub boot menu will always be displayed on boot (5s timeout)
- Security hardening configs
- Git: 
  - sets up git username & email
  - add git config file with defaults & settings
  - [SCM Breeze](https://github.com/scmbreeze/scm_breeze)
- Docker: install docker
- DNS: adds [DNS blacklist](https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts) 
  which maps advertising and tracking hosts to '0.0.0.0'
- Apt: installs a lot of packages, eg: clamav, zip, shellcheck
- VIM: deploys vimrc file
- Apps:
   - Brave
   - Intellij (ultimate)
   - Steam
  
## Remove List

- Boiler plate directories, eg: ~/Documents
- apparmor
- firefox


## Manual Install

- set up keyboard shortcuts
- [yed](https://www.yworks.com/products/yed/download)

### Git Tools

```
git clone git@github.com:DanVanAtta/git_tools.git ~/.git_tools

## add to path
grep -q 'git_tools' ~/.bashrc \
    || (TOOL_HOME=~/.git_tools \
          && echo -n 'PATH=$PATH:' >> ~/.bashrc \
          && echo "$TOOL_HOME" >> ~/.bashrc)
```

