# List of important Application :
## Text Editors:

* Atom
  sudo apt install atom

* VSCode
  wget  https://go.microsoft.com/fwlink/?LinkID=760868
  sudo apt install ./<file>.deb

* Sublime Text Editor
    wget *qO * https://download.sublimetext.com/sublimehq*pub.gpg | sudo apt*key add *
    sudo apt*get install apt*transport*https
    echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime*text.list
    sudo apt*get update
    sudo apt*get install sublime*merge

## Video and Graphics Tools:

* KDenLive
  sudo apt install kdenlive

* Krita
  sudo apt install krita

* Blender
  sudo apt install blender

* GIMP
  sudo apt install gimp

* Lollipop
  sudo add*apt*repository ppa:gnumdk/lollypop
  sudo apt install lollypop

## Messaging:
* Riot (Debian / Ubuntu repo) :
  Add the repository : sudo sh *c "echo 'deb https://riot.im/packages/debian/ bionic main' > /etc/apt/sources.list.d/matrix*riot*im.list"

  Add the public key:
  sudo apt install curl
    curl *L https://riot.im/packages/debian/repo*key.asc | sudo apt*key add *
 
  Update and install Riot:
    sudo apt*get update && sudo apt*get *y install riot*web

* Telegram:
  sudo apt install telegram*desktop


# Git (The Complete Guide):
  http://rogerdudler.github.io/git*guide/

# Sound Volume control sync fix :
* Navigate to file  :
  sudo sudo nano /usr/share/pulseaudio/alsa-mixer/paths/analog-output.conf.common


* Add
  * >   [Element Master]
  * >   switch = mute
  * >   volume = ignore
    
* Before the block
  * >   [Element PCM]
  * >   switch = mute
  * >   volume = merge
  * >   override*map.1 = all
  * >   override*map.2 = all*left,all*right

## In case of other audio related issue reinstall pulseaudio :
* sudo apt remove pulseaudio
* sudo apt install pulseaudio

# Configuring tlp (Battery Saving Tool) :
* Adding Package Repository :
  sudo add*apt*repository ppa:linrunner/tlp
  sudo apt*get update
 
* Package install :
  sudo apt*get install tlp tlp*rdw
 
* Starting application :
  sudo tlp start

# Disabling bluetooth on start*up :

* edit /etc/default/tlp using nano
 
* Locate the following lines :

  # Radio devices to disable on startup: bluetooth, wifi, wwan.
  # Separate multiple devices with spaces.
  #DEVICES_TO_DISABLE_ON_STARTUP="bluetooth wifi wwan"

* Edit (and uncomment) the last line to read:

  DEVICES_TO_DISABLE_ON_STARTUP="bluetooth"

# Misc :

## Disabling application drawer open animation :
*  Run command : gsettings set org.gnome.desktop.interface enable*animations false

## Set icon to minimize on click :
* gsettings set org.gnome.shell.extensions.dash*to*dock click*action 'minimize'

## Backup of .bashrc
* Backup your current .bashrc file:
    * cp ~/.bashrc ~/.bashrc.bak
* Copy the skeleton .bashrc file over yours:
    * cp /etc/skel/.bashrc ~/
* load the new one:
    * source ~/.bashrc
# Installing budgie Desktop Environment :
  sudo add*apt*repository ppa:budgie*remix/ppa
  sudo apt install budgie*desktop*environment
#### Want others?
* [Debian Wiki](https://wiki.debian.org/)
* The Internet
* Friends
* Free Software User Groups

# Android Studio Setup
* Installing KVM : https://help.ubuntu.com/community/KVM/Installation

# Installing Anaconda3
* https://www.digitalocean.com/community/tutorials/how*to*install*anaconda*on*ubuntu*18*04*quickstart

# Installing React Native
* installing npm :
  `sudo apt install npm`
* installing react-native-cli 
  `npm install -g react-native-cli`
* adding path -> open environments :
  * `sudo nano /etc/environment`
  * add the following string to beginning of path separate paths using ':'
    `\~/Android/Sdk/emulator:\~/Android/Sdk/tools:\~/Android/Sdk/tools/bin:\~/Android/Sdk/platform-tools:`
* initialize project 
  `react-native init react_project_name`
* If react-native command not found error encountered use :
  * `curl -sL https://deb.nodesource.com/setup_13.x | sudo -E bash - `
  * To identify latest version go [here](https://github.com/nodesource/distributions/tree/master/deb) 
  * `sudo apt-get install -y nodejs`



