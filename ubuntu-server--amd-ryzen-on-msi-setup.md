## How-To: Install Ubuntu-Server 22.04 & then Update to Desktop 22.10

### Hardware

- Ryzen 7950x
- MSI PRO X670-P WIFI


### BIOS Settings

- Ensure 'uefi' is enabled before installing OS
- Turn off all overclocking (lots of instability with 'AMD overclocking' turned on)
- Secure boot off
- UEFI USB key to highest boot priority

### Install OS (ubuntu-server to desktop)

Had issues with USB install and needed to install an OS under 2GB (largest USB key I had on hand).
To do this, download the ubuntu-server ISO and load it on the USB key

### Install Ubuntu 22.04 (server)

Download ISO, flash to a USB key, boot from USB key, select minimal server. Once rebooted & logged into CLI:

```
sudo apt install ubuntu-desktop
sudo apt install gdm3 vim
sudo vi /etc/gdm3/custom.conf
  # Set the following: 'WaylandEnabled=true'
sudo update-grub2
```

### Install packages not available on the very minimal server install
```
sudo apt whiptail ip-utils rsyslog python3 python3-is-python htop 
```

### Start up Desktop GUI

```
sudo systemctl start gdm3
```

### Upgrade to Ubuntu 22.10

```
sudo ubuntu-drivers autoinstall
```

### Fix Fonts

Add the following to `/etc/profile`

```
export FONTCONFIG_PATH=/etc/fonts
```

### Application installs

Brave: https://brave.com/linux/

```
sudo snap install steam
sudo snap install intellij-idea-ultimate --classic
```
