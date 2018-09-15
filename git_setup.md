## ssh key
```
ssh-keygen -t ed25519
```

## GPG Key

- [generate gpg key](https://help.github.com/articles/generating-a-new-gpg-key/)
- [add key to git](https://help.github.com/articles/telling-git-about-your-gpg-key/)



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
