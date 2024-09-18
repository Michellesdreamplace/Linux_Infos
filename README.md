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
### ⚙️ Eintragungen in der '/etc/apt/sources.list':
```
# bookworm-backports, previously on backports.debian.org
deb http://deb.debian.org/debian bookworm-backports main contrib non-free non-free-firmware  
deb-src http://deb.debian.org/debian bookworm-backports main contrib non-free non-free-firmware  

# multimedia repository
deb https://www.deb-multimedia.org bookworm main non-free
deb https://www.deb-multimedia.org bookworm-backports main non-free
```
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ 
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
- Debian Multimedia installieren (v2):
```
echo "## Multimedia Repo" | sudo tee /etc/apt/sources.list.d/deb-multimedia.list
echo "deb https://www.deb-multimedia.org bookworm main non-free" | sudo tee -a /etc/apt/sources.list.d/deb-multimedia.list
sudo apt install -y wget apt-transport-https
wget https://www.deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
sudo dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
sudo apt update -y
```

 ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀ ⠀
 
