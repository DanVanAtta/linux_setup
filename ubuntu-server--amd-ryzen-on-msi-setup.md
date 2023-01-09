## How-To: Install Ubuntu-Server 22.04 & then Update to Desktop 22.10

Needed some special steps to get some new hardware running. This documents those
steps  and installing Ubuntu Desktop from an Ubuntu-Server installation.

### Hardware

- Ryzen 7950x
- MSI PRO X670-P WIFI

### Flash BIOS

<http://service.msicomputer.com/msi_user/support/ts_general_form.aspx?case_id=22032799&email=dhvatta%40gmail.com&pclass=MB>

I was getting  a 'red light' on the motherboard for CPU & 'yellow light' for RAM. Following
the above steps, the flash did not seem to succeed (and took not very long, not the 10 minutes
that the vido cautions), but it did do the trick and allowed the system to boot.


### Update BIOS

[Steps missing..]

BIOS updates were strongly needed for everything to work properly.

### BIOS Settings

- Ensure 'uefi' is enabled before installing OS
- Turn off all overclocking (lots of instability with 'AMD overclocking' turned on)
- Secure boot off
- UEFI USB key set to highest boot priority

### Install OS (ubuntu-server to desktop)

The largest USB key I had on hand was 2GB. The only Ubuntu image smaller than that is the 'server' image.
The steps below are for installing from this server image (which is nice and extra minimal).

### Install Ubuntu 22.04 (server)

Download ISO, flash to a USB key, boot from USB key, select minimal server. Once rebooted & logged into CLI:

```
sudo apt install ubuntu-desktop gdm3 vim
sudo update-grub2
```

### Start up Desktop GUI

```
sudo systemctl start gdm3
```

## Next Steps (Ubuntu-Desktop now working!)

- log into the system
- run the system setup (see the main <README.md>)
- do a reboot
- run the below fixes


### Fix Fonts

Add the following to `/etc/profile`
```
export FONTCONFIG_PATH=/etc/fonts
```

### Install drivers
```
sudo ubuntu-drivers autoinstall
```

### Install linux AMD GPU firmware

```
git clone https://kernel.googlesource.com/pub/scm/linux/kernel/git/firmware/linux-firmware.git
sudo cp linux-firmware/amdgpu/* /lib/firmware/amdgpu && sudo update-initramfs -k all -u -v
```
