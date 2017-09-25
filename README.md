```
ssh-keygen

## upload key to github

sudo apt-get install git -y

git clone git@github.com:DanVanAtta/linux_setup.git
cd linux_setup

./harden_kernel
./apt_install
./git_setup "[Name]" "[email]"
./scm_breeze
./etc_host_ad_block

```


### Git Commit Signing GPG Key Setup
- [generate gpg key](https://help.github.com/articles/generating-a-new-gpg-key/)
- [add key to git](https://help.github.com/articles/telling-git-about-your-gpg-key/)


### Apps to install

- [yed](https://www.yworks.com/products/yed/download)
- [mysql workbench](http://dev.mysql.com/downloads/workbench/)
- [intellij](https://www.jetbrains.com/idea/download/#section=linux)

## More Settings

- Appearance > Behavior
  - enable workspaces
  - auto-hide launcher = on
  - reveal sensitivity -> higher
  - Brightness and lock
  - turn screen off > 30 minutes
- Security and Privacy
  - Files and Applications
    - record file and application usage > off
  - Search
    - include online search results > off
