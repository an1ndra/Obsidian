### Extentions
- Floating Dock
- GSconnect
- GTK title bar
- Hide top bar
- Sound input and Out put Chooser
- User Themes
- ----
- Pop shell
- pop Shop Details
- System76 power
- Ubuntu Applndicators

### Applications
- Update KDE
```bash
sudo pkcon refresh && sudo pkcon update
```
- zsh
```bash
	sudo apt install zsh
```
- Java
```bash
	sudo apt-get install openjdk-8-jdk
	export JAVA\_HOME = /usr/lib/jvm/java-8-openjdk	
	export PATH = $PATH:/usr/lib/jvm/java-8-openjdk/bin
```
- Discord
	
```bash
	https://discord.com/api/download?platform=linux&format=deb
	sudo apt install ./discord-0.0.13.deb
```
- Telegram
```bash
	sudo apt install telegram-dekstop
	
	sudo add-apt-repository ppa:atareao/telegram
	sudo apt update && sudo apt install telegram
```
- Obs
```bash
	sudo add-apt-repository ppa:obsproject/obs-studio
	sudo apt update
	sudo apt install obs-studio
```
- Spotify
```bash
	curl -sS https://download.spotify.com/debian/pubkey\_0D811D58.gpg | sudo apt-key add -   
	echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
	sudo apt-get update && sudo apt-get install spotify-client
```
- VLC
```bash
	sudo apt install vlc	
```
- VScode
```bash
	sudo apt install vscode
```
- AndroiStudio
```bash
	https://redirector.gvt1.com/edgedl/android/studio/ide-zips/4.2.1.0/android-studio-ide-202.7351085-linux.tar.gz
```
- Brave
```bash
	sudo apt install apt-transport-https curl
	sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
	echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
	sudo apt update
	sudo apt install brave-browser
```
- Obsidian
```bash
	wigethttps://github.com/obsidianmd/obsidian-releases/releases/download/v0.9.20/obsidian_0.9.20_amd64.deb
```
- Dropbox
```bash
	https://www.dropbox.com/download?dl=packages/ubuntu/dropbox_2020.03.04_amd64.deb
```
- Intellij IDE
- Krita
```bash
	sudo add-apt-repository ppa:kritalime/ppa
	sudo apt update
	sudo apt-get install krita
```
- Vim
```bash
	sudo apt install vim
```
- Zoom
- Publii
- Insmonia
- Pycharm
- XFC terminal
- Virtual Box
- Stacher
```bash
	https://github.com/oguzhaninan/Stacer
```
- Firefox 
```bash
	sudo apt install firefox
```

------
Install VScode in pop os wothout downgrade VScode
```bash
sudo vim /etc/apt/preferences.d/pop-default-settings
Package: code
Pin: origin packages.microsoft.com
Pin-Priority: 9999
```
Install VScodium in Pop os without downgrade VScodium
```bash
sudo vim /etc/apt/preferences.d/pop-default-settings
Package: codium
Pin: origin "paulcarroty.gitlab.io"
Pin-Priority: 9999
```
install Spotify in Pop os
http://repository.spotify.com stable non-free
```bash
sudo vim /etc/apt/preferences.d/pop-default-settings
Package: spotify-client
Pin: origin "repository.spotify.com"
Pin-Priority: 9999
```

Spotify adblock
```bash
https://github.com/MrTuNNe/Spotify-AdBlocker/blob/master/spotify_adblock.py
```