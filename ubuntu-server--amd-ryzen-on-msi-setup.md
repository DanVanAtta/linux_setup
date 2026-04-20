
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
