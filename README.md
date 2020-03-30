# Installation

## Installing:
### Install pre-requisite
```
$ flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
$ flatpak install flathub org.gnome.Platform//3.36 org.gnome.Sdk//3.36 --system
```

### Clone
Do not download the ZIP file as it doesn't contain the required files from _shared-modules_ repository.  
Instead, do:
```
git clone --recurse-submodules https://github.com/dgcampea/desmume-flatpak.git
```

### Build + Install
```
$ flatpak-builder builddir org.desmume.DeSmuME.yaml --force-clean --install --user
```

## Notes:
By default, this flatpak only allows reading from **HOME** and saving to **XDG-VIDEOS** and **XDG-MUSIC** directories.  
If you want to save/read from other locations:
```
flatpak override org.desmume.DeSmuME --filesystem=host
```

### Where are my savefiles?
Located at `~/.var/app/org.desmume.DeSmuME/config/desmume/`
