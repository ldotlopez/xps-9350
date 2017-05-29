Packages
===


Desktop
---
banshee shotwell
gnome-tweak-tool
network-manager-openvpn-gnome
network-manager-vpnc-gnome 
nautilus-dropbox
terminator
ubuntu-restricted-addons
dconf-editor
gconf-editor
d-feet 


Tools
---
apt-file
curl
git
gpm 
htop
iftop
iotop
moreutils
vim
virtualenvwrapper


Remove
---
gnome-music
gnome-photos
gnome-documents 
rhythmbox
snapd
snapd-login-service 


Repos
===

Spotify
---
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt-get update && sudo apt-get install spotify-client

Resilio Sync
---
wget -qO - https://linux-packages.resilio.com/resilio-sync/key.asc | sudo apt-key add -
echo "deb http://linux-packages.resilio.com/resilio-sync/deb resilio-sync non-free" | sudo tee /etc/apt/sources.list.d/resilio-sync.list
sudo apt-get update && sudo apt-get install resilio-sync

Gnome Pomodoro
---
wget -qO - http://download.opensuse.org/repositories/home:kamilprusko/xUbuntu_16.10/Release.key | sudo apt-key add -
echo 'deb http://download.opensuse.org/repositories/home:kamilprusko/xUbuntu_16.10/ /' | sudo tee /etc/apt/sources.list.d/gnome-pomodoro.list
sudo apt-get update && sudo apt-get install gnome-pomodoro

Slack
---
https://slack.com/downloads/instructions/linux


Gnome-Shell extensions
===

* Installed by default

Alternate Tab - https://extensions.gnome.org/extension/15/alternatetab/
Auto Move Windows - https://extensions.gnome.org/extension/16/auto-move-windows/
Removable Drive Menu - https://extensions.gnome.org/extension/7/removable-drive-menu/
Launch New Instance - https://extensions.gnome.org/extension/600/launch-new-instance/

* From extensions.gnome.org

Dash to Dock - https://extensions.gnome.org/extension/307/dash-to-dock/
cpufreq - https://extensions.gnome.org/extension/1082/cpufreq/
Media Player Indicator - https://extensions.gnome.org/extension/55/media-player-indicator/
Switcher - https://extensions.gnome.org/extension/973/switcher/
Top Icons Plus - https://extensions.gnome.org/extension/1031/topicons/
WindowOverlay Icons - https://extensions.gnome.org/extension/302/windowoverlay-icons/

Hacks
===


Set default editor to vim
---
  * `sudo update-alternatives --set editor $(realpath /usr/bin/vim)`


rslsync as user
---

  * Copy rslsync files to /etc/systemd/system and /etc/systemd/user
  * `systemctl --user enable "rslsync@$USER"`


A2DP Bluetooth profile doesn't work with gdm
---
  * Install file: var-lib-gdm3-.config-pulse-client.conf

