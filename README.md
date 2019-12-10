```
ssh-keygen -t ed25519
sudo apt install -y git ansible
rmdir Videos/ Templates/ Music/ Pictures/ Documents/ Public/
mkdir work/
cd work/
git clone https://github.com/DanVanAtta/linux_setup.git
git clone git@github.com:DanVanAtta/linux_setup.git
cd linux-setup/
./run-ansible
```

- [Choose fastest mirror](https://linuxconfig.org/things-to-do-after-installing-ubuntu-18-04-bionic-beaver-linux)

### Apps to install


## Also to install 

- [generate gpg key](https://help.github.com/articles/generating-a-new-gpg-key/)
- [add key to git](https://help.github.com/articles/telling-git-about-your-gpg-key/)
- [sign commits](https://help.github.com/articles/signing-commits/)


## ssh key
```
ssh-keygen -t ed25519
```

## GPG Key

- [generate gpg key](https://help.github.com/articles/generating-a-new-gpg-key/)
- [add key to git](https://help.github.com/articles/telling-git-about-your-gpg-key/)
- [sign commits](https://help.github.com/articles/signing-commits/)

Add alias:
```
alias gc='git commit -S'

```

## SCM breeze https://github.com/ndbroadbent/scm_breeze
```
git clone git://github.com/ndbroadbent/scm_breeze.git ~/.scm_breeze
~/.scm_breeze/install.sh
source ~/.bashrc
```

## Git Tools


```
git clone git@github.com:DanVanAtta/git_tools.git ~/.git_tools

## add to path
grep -q 'git_tools' ~/.bashrc \
    || (TOOL_HOME=~/.git_tools \
          && echo -n 'PATH=$PATH:' >> ~/.bashrc \
          && echo "$TOOL_HOME" >> ~/.bashrc)
```

## Git config

```
export GIT_NAME=
export GIT_EMAIL=

git config --global user.email "$GIT_EMAIL"
git config --global user.name "$GIT_NAME"

git config --global core.editor vi
git config --global merge.tool meld
git config --global core.autocrlf input
git config branch.autosetuprebase always --global
git config --global push.default simple
git config --global core.pager "diff-so-fancy | less --tabs=2 -RFX"

# fancy diff color
git config --global color.diff-highlight.oldNormal "red bold"
git config --global color.diff-highlight.oldHighlight "red bold 52"
git config --global color.diff-highlight.newNormal "green bold"
git config --global color.diff-highlight.newHighlight "green bold 22"
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
sudo apt-get remove apparmor apparmor-utils -y


# firewall
sudo ufw enable

# allow ssh
sudo ufw limit ssh
sudo ufw allow 22

## tripleA port
sudo ufw allow 3300
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
- [intellij](https://www.jetbrains.com/idea/download/#section=linux)
