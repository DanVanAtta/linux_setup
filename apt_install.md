```
sudo apt-get update

sudo apt install -y npm vim gimp htop traceroute clamav shellcheck fail2ban \
  nmap git google-chrome-stable unrar zip unzip \
  sharutils rar file-roller ruby ruby-dev libxml2-utils
  
sudo npm install -g diff-so-fancy
sudo gem install travis -v 1.8.2 --no-rdoc --no-ri
sudo apt -y upgrade
sudo apt autoremove -y
```

### Docker

```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
apt-cache policy docker-ce
sudo apt install docker-ce
```

### Java 8

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt update
sudo apt install oracle-java8-installer
```
