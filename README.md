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

- Git: sets up git username & email
- Git: adds config file with git defaults & settings
- Docker: installs sudo-less docker
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



## SCM breeze

```
git clone git@github.com:scmbreeze/scm_breeze.git ~/.scm_breeze
~/.scm_breeze/install.sh
```

```
git clone git@github.com:DanVanAtta/git_tools.git ~/.git_tools

## add to path
grep -q 'git_tools' ~/.bashrc \
    || (TOOL_HOME=~/.git_tools \
          && echo -n 'PATH=$PATH:' >> ~/.bashrc \
          && echo "$TOOL_HOME" >> ~/.bashrc)
```


```
## warning, the above may remove 'snap' (that is not desirable)
## re-install snap with: sudo apt install -y snapd
```

Also:
- set up keyboard shortcuts
- run ubuntu software updater
- [yed](https://www.yworks.com/products/yed/download)
- install intellij with snap 
