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