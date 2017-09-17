Software
===

Desktop
---
* banshee
* dconf-editor gconf-editor
* d-feet 
* gnome-tweak-tool
* mplayer
* network-manager-openvpn-gnome network-manager-vpnc-gnome 
* nautilus-dropbox
* pdfmod
* shotwell
* terminator
* ubuntu-restricted-addons


Tools
---
* apt-file
* curl
* git
* gpm
* htop
* iftop
* iotop
* moreutils
* pmount
* vim
* virtualenvwrapper


Remove
---
* gnome-documents gnome-music gnome-photos
* rhythmbox
* snapd snapd-login-service


Non apt software
===

Gnome Pomodoro
---

    wget -qO - http://download.opensuse.org/repositories/home:kamilprusko/xUbuntu_16.10/Release.key| sudo apt-key add -
    echo 'deb http://download.opensuse.org/repositories/home:kamilprusko/xUbuntu_16.10 | sudo tee /etc/apt/sources.list.d/gnome-pomodoro.list
    sudo apt-get update && sudo apt-get install gnome-pomodoro


Gnome Shell
---
* [Alternate Tab](https://extensions.gnome.org/extension/15/alternatetab/) *(Installed by default)*
* [Auto Move Windows](https://extensions.gnome.org/extension/16/auto-move-windows/) *(Installed by default)*
* [Removable Drive Menu](https://extensions.gnome.org/extension/7/removable-drive-menu/) *(Installed by default)*
* [Launch New Instance](https://extensions.gnome.org/extension/600/launch-new-instance/) *(Installed by default)*
* [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock)
* [cpufreq](https://extensions.gnome.org/extension/1082/cpufreq/)
* [Media Player Indicator](https://extensions.gnome.org/extension/55/media-player-indicator/)
* [Switcher](https://extensions.gnome.org/extension/973/switcher/)
* [Top Icons Plus](https://extensions.gnome.org/extension/1031/topicons/)
* [WindowOverlay Icons](https://extensions.gnome.org/extension/302/windowoverlay-icons/)


Spotify
---

    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886
    echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list
    sudo apt-get update && sudo apt-get install spotify-client


Resilio Sync
---

    wget -qO - https://linux-packages.resilio.com/resilio-sync/key.asc | sudo apt-key add -
    echo "deb http://linux-packages.resilio.com/resilio-sync/deb resilio-sync non-free | sudo tee /etc/apt/sources.list.d/resilio-sync.list
    sudo apt-get update && sudo apt-get install resilio-sync


Slack
---
[Download](https://slack.com/downloads/instructions/linux)


Sublime
---
[Download](https://www.sublimetext.com/3)



Hacks
===


Set default editor to vim
---
  * `sudo update-alternatives --set editor $(realpath /usr/bin/vim)`


rslsync as user
---

  * Install files:
    * `etc-systemd-system-rslsync.service`
    * `etc-systemd-user-rslsync@.service`
  * `systemctl daemon-reload`
  * `systemctl --user enable "rslsync@$USER"`


A2DP Bluetooth profile doesn't work with Gnome
---

Install file: `var-lib-gdm3-.config-pulse-client.conf`

[https://wiki.debian.org/BluetoothUser/a2dp](https://wiki.debian.org/BluetoothUser/a2dp)


Wifi doesn't work after sleep
---

Install files:

  * `usr-local-bin-xps-9350-reload-wifi-modules`
  * `lib-systemd-system-sleep-xps-9350-reload-wifi-modules`


Configure official DELL dock
---

Install files:

  * `usr-local-bin-xps-9350-autoconfigure-dock`

