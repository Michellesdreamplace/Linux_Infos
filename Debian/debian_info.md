# ![](https://github.com/Michellesdreamplace/Linux_Infos/blob/main/pix/icons_64x64/Debian.png)⠀ ⠀Debian Stable Infos
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
### 🔗 meine persönliche Linksammlung zu Debian:
- [DEBIAN: Homepage & download](https://www.debian.org/)
- [DEBIAN: download - daily-image amd64 netboot mini.iso](https://d-i.debian.org/daily-images/amd64/daily/netboot/mini.iso)
- [DEBIAN: download - Offizielle Live-Installations-Images für die Stable-Veröffentlichung](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/)
- [FAI.me: Build your own installation ISO for Debian](https://fai-project.org/FAIme/)  
- [DEBIAN: Paketsuche](https://packages.debian.org/de/)
- [debianforum](https://debianforum.de/)
- [DEBIAN: wiki - WLAN Einrichten](https://wiki.debianforum.de/WLAN_Einrichten)
- [DEBIAN: wiki - Unfreie Grafiktreiber für NVIDIA](https://wiki.debianforum.de/Unfreie_Grafiktreiber_f%C3%BCr_NVIDIA)
- [DEBIAN: wiki - NVIDIA Proprietary Driver](https://wiki.debian.org/NvidiaGraphicsDrivers)
- [DEBIAN: howto - Debian auf btrfs, fein gewürzt mit Timeshift – ein Serviervorschlag von SaintofSinner](https://saintofsinner.de/debian-auf-btrfs-fein-gewuerzt-mit-timeshift-ein-serviervorschlag/)⠀ ⠀ *(für erfahrene Nutzer)* 
- [FONT: Clear Sans](https://www.fontsquirrel.com/fonts/clear-sans)
- [FONT: Download-Seite für ttf-mscorefonts-installer](https://packages.debian.org/de/sid/all/ttf-mscorefonts-installer/download)
```
sudo dpkg --install /PFAD/ZUR/PAKETDATEI/ttf-mscorefonts-installer_3.8.1_all.deb
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
______________________________________________________________________________________________________
### ⚙️ Eintragungen in der '/etc/apt/sources.list' der Debian-Stable-Version:
```
deb https://deb.debian.org/debian/ bookworm main non-free-firmware contrib non-free
deb-src https://deb.debian.org/debian/ bookworm main non-free-firmware contrib non-free

deb https://deb.debian.org/debian/ bookworm-security main non-free-firmware contrib non-free
deb-src https://deb.debian.org/debian/ bookworm-security main non-free-firmware contrib non-free

# bookworm-updates, um Updates zu erhalten, bevor eine Zwischenveröffentlichung veröffentlicht wird;
# siehe https://www.debian.org/doc/manuals/debian-reference/ch02.en.html#_updates_and_backports
deb https://deb.debian.org/debian/ bookworm-updates main non-free-firmware contrib non-free
deb-src https://deb.debian.org/debian/ bookworm-updates main non-free-firmware contrib non-free

# bookworm-backports, zuvor auf backports.debian.org
deb http://deb.debian.org/debian bookworm-backports main non-free-firmware contrib non-free
deb-src http://deb.debian.org/debian bookworm-backports main non-free-firmware contrib non-free
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
______________________________________________________________________________________________________
### ⚙️ diverse Shell-Befehle:
 ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian System auf [deutsch](https://wiki.debian.org/de/HowTo/Install/Deutsch) umstellen:
```
sudo apt install task-german
sudo dpkg-reconfigure locales
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 - Die schnellsten 20 Spiegelserver für Debian *bookworm* finden. [🔗](https://book.dpmb.org/debian-paketmanagement.chunked/ch03s06.html)⠀ *(gewünschten dann in die '/etc/apt/sources.list' eintragen)*:
```
sudo apt install netselect-apt
sudo netselect-apt -c germany -t 20 -a amd64 -n bookworm
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian update & upgrade:
```
sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y && sudo apt clean -y && sudo apt autoclean -y && sudo apt autoremove -y
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ 
- ⚠️ Debian backport-Pakete installieren⠀ (die '/etc/apt/sources.list' muss dafür angepasst sein):
```
sudo apt install -t bookworm-backports libreoffice libreoffice-l10n-de libreoffice-help-de
```
```
sudo apt search -t bookworm-backports nvidia
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 - Debian zusätzliche Software installieren:
```
sudo apt install timeshift backintime-qt backintime-common thunderbird thunderbird-l10n-de keepassxc gparted transmission-gtk vlc pavucontrol geany gimp inkscape audacity filezilla ffmpeg default-jdk git wget nano vim htop neofetch screenfetch tasksel locate p7zip p7zip-full tar rar unrar unzip ufw gufw flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
sudo flatpak update -y
sudo apt install flatpak gnome-software-plugin-flatpak -y
sudo flatpak install flathub com.github.tchx84.Flatseal -y
sudo flatpak install flathub com.mattjakeman.ExtensionManager -y
sudo apt update -y
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
  - Debian Grafikkarten Treiber NVIDIA installieren:
```
sudo apt update
sudo apt install nvidia-detect -y
nvidia-detect
sudo apt install nvidia-driver firmware-misc-nonfree
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
   - Debian Grafikkarten Treiber AMD installieren:
```
sudo apt purge *nvidia*
sudo apt install firmware-amd-graphics libgl1-mesa-dri libglx-mesa0 mesa-vulkan-drivers xserver-xorg-video-all
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian-Stable Multimedia installieren (incl. anlegen der Repo):
```
echo "# multimedia repository" | sudo tee /etc/apt/sources.list.d/deb-multimedia.list
echo "deb https://www.deb-multimedia.org bookworm main non-free" | sudo tee -a /etc/apt/sources.list.d/deb-multimedia.list
echo "deb https://www.deb-multimedia.org bookworm-backports main non-free" | sudo tee -a /etc/apt/sources.list.d/deb-multimedia.list
sudo apt install -y wget apt-transport-https
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
sudo apt update -y
sudo apt upgrade -y
```
*folgendes sollte dann in der '/etc/apt/sources.list.d/deb-multimedia.list' stehen:*
```
# multimedia repository
deb https://www.deb-multimedia.org bookworm main non-free
deb https://www.deb-multimedia.org bookworm-backports main non-free
```  
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀   
______________________________________________________________________________________________________
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
# ![](https://github.com/Michellesdreamplace/Linux_Infos/blob/main/pix/icons_64x64/Debian.png)⠀ ⠀Debian SID Infos
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
### ⚙️ Eintragungen in der '/etc/apt/sources.list' der Debian-SID-Version:
```
deb http://deb.debian.org/debian/ sid main contrib non-free non-free-firmware  
deb-src http://deb.debian.org/debian/ sid main contrib non-free non-free-firmware  
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
______________________________________________________________________________________________________
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian-SID Multimedia installieren (incl. anlegen der Repo):
```
echo "# multimedia repository" | sudo tee /etc/apt/sources.list.d/deb-multimedia.list
echo "deb https://www.deb-multimedia.org sid main non-free" | sudo tee -a /etc/apt/sources.list.d/deb-multimedia.list
sudo apt install -y wget apt-transport-https
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
sudo apt update -y
sudo apt upgrade -y
```
*folgendes sollte dann in der '/etc/apt/sources.list.d/deb-multimedia.list' stehen:*
```
# multimedia repository
deb https://www.deb-multimedia.org sid main non-free
```
