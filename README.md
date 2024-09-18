# ℹ️ Infos
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
### 🔗 meine persönliche Linksammlung:
- [DEBIAN: download - daily-image amd64 netboot mini.iso](https://d-i.debian.org/daily-images/amd64/daily/netboot/mini.iso)  
- [DEBIAN: wiki - NVIDIA Proprietary Driver](https://wiki.debian.org/NvidiaGraphicsDrivers)  
- [DEBIAN: howto - Debian auf btrfs, fein gewürzt mit Timeshift – ein Serviervorschlag von SaintofSinner](https://saintofsinner.de/debian-auf-btrfs-fein-gewuerzt-mit-timeshift-ein-serviervorschlag/)  
- [FONT: Clear Sans](https://www.fontsquirrel.com/fonts/clear-sans)  
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
______________________________________________________________________________________________________
### ⚙️ Eintragungen in der '/etc/apt/sources.list':
```
# bookworm-backports, previously on backports.debian.org
deb http://deb.debian.org/debian bookworm-backports main contrib non-free non-free-firmware  
deb-src http://deb.debian.org/debian bookworm-backports main contrib non-free non-free-firmware  
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
### ⚙️ Eintragungen in der '/etc/apt/sources.list.d/deb-multimedia.list':
```
# multimedia repository
deb https://www.deb-multimedia.org bookworm main non-free
deb https://www.deb-multimedia.org bookworm-backports main non-free
```
danach folfendes im Terminal:
```
sudo apt install -y wget apt-transport-https
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
sudo apt update -y
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
______________________________________________________________________________________________________
### ⚙️ diverse Shell-Befehle:
 ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian backport-Paket installieren:
```
sudo apt install -t bookworm-backports <package>
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
 ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian Multimedia installieren:
```
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
apt-get update
```
 ⠀ ⠀ ⠀ ⠀ ⠀ 
  ⠀ ⠀ ⠀ ⠀ ⠀ 
- Debian Multimedia installieren (incl. anlegen der Repo):
```
echo "## Multimedia Repo" | sudo tee /etc/apt/sources.list.d/deb-multimedia.list
echo "deb https://www.deb-multimedia.org bookworm main non-free" | sudo tee -a /etc/apt/sources.list.d/deb-multimedia.list
sudo apt install -y wget apt-transport-https
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
sudo apt update -y
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
 - Debian zusätzliche Software installieren:
```
sudo apt install timeshift thunderbird thunderbird-l10n-de keepassxc gparted transmission-gtk vlc pavucontrol geany gimp inkscape audacity filezilla leafpad ffmpeg default-jdk git wget nano vim htop neofetch screenfetch tasksel locate p7zip p7zip-full tar rar unrar unzip ufw gufw flatpak
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
______________________________________________________________________________________________________
