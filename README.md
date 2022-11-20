```
git clone git@github.com:DanVanAtta/linux_setup.git
./run-ansible
```

- [Choose fastest mirror](https://linuxconfig.org/things-to-do-after-installing-ubuntu-18-04-bionic-beaver-linux)


## ssh key
```
ssh-keygen -t ed25519
```


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
sudo sed -i 's/\(kernel.kptr_restrict = \).*/\12/' /etc/sysctl.d/10-kernel-hardening.conf

# set all desktop start up to not be hidden
sudo sed -i 's/NoDisplay=true/NoDisplay=false/g' /etc/xdg/autostart/*.desktop

# disallow ssh password login
sudo sed -i 's/^#\(.*PasswordAuthentication\) .*/\1 no/' /etc/ssh/ssh_config

# remove app armor 
service apparmor stop
update-rc.d -f apparmor remove
sudo apt-get remove apparmor apparmor-utils

## warning, the above may remove 'snap' (that is not desirable)
## re-install snap with: sudo apt install -y snapd

# firewall
sudo ufw enable
```

```
cd ~
rmdir Documents/ Music/ Pictures/ Public/ Templates/ Videos/
mkdir work/
```

Also:
- set up keyboard shortcuts
- run ubuntu software updater
- [yed](https://www.yworks.com/products/yed/download)
- install intellij with snap 
