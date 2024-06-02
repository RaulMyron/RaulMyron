## Dracula Theme

```bash
sudo apt update
sudo apt-get install dconf-cli
git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal
./install.sh
```
## Show Branch

```bash
code ~/.bashrc
```

Find “PS1” in .bashrc like:
```bash
if [ "$color_prompt" = yes ]; then 
PS1= ...
else 
    PS1= ...
fi 
```
instead of above lines, paste blow lines
```bash
# git branch info if present
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}


if [ "$color_prompt" = yes ]; then
   PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[33m\]$(parse_git_branch)\[\033[00m\]\$ '
else
   PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w$(parse_git_branch)\$ '
fi
```


