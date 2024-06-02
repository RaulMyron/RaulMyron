# Settings things up for a clean installation of ubuntu

```bash
sudo apt-get update
sudo apt-get upgrade
```

## For basic software I like to use the app center, just a list for my remembering:
1. Brave
2. VSCODE
3. Discord
4. Spotify


## For aesthestics
I like to use ```gnome-tweaks``` and tho it's broken in the latest ubuntu 24 release so I'm avoiding it,
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top true #for bottom left show apps
sudo apt install gnome-tweaks
```

## For mice/mouse
I like to use the piper instead of the ubuntu software but I use a mainstream mouse, so be aware.
```bash
sudo apt install ratbagd
sudo apt install piper
piper
```
## Remeber to set up Git SSH key onto this (link)[https://github.com/RaulMyron/RaulMyron/blob/main/SSHgithub.md]

## Remeber to set up branch Terminal (link)[https://github.com/RaulMyron/RaulMyron/blob/main/BranchTerminal.md]

## Some software update just for better use onto Ubuntu
```bash
sudo apt-get remove --auto-remove brltty
sudo apt-get install python3-virtualenv
`` 
