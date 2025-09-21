# Yocto-BBlayers&Packages

## BBlayers

- Checked for exsiting layers.
```bash
bitbake-layers show-layers
```
- Removed a layer.
```bash
bitbake-layers remove-layer meta-raspberrypi/
```
- Readded the removed layer.
```bash
bitbake-layers add-layer meta-raspberrypi/
```

## Packages

- Initalized environment.
```bash
source oe-init-build-env ../builds/pi
```
- Checked the recipes.
```bash
bitbake-layers show-recipes #Showed everything 🫠
```
- Checked only the recipes I wanted to pre-install with image.
```bash
bitbake-layers show-recipes python3 git
```
- Made sure meta layer is present in `bblayers.conf`.
- Edited local.conf file:
```bash
IMAGE_INSTALL:append = " python3 git"
```
- Built Image to include the new packages `python3` and `git`.
- Checked if they were added using:
```bash
bitbake -e core-image-full-cmdline | grep "^IMAGE_INSTALL="
oe-pkgdata-util list-pkgs | egrep "git|python3"
```
- Flased the image onto pi 5 and booted it successfully.
- Checked if the the packages where installed.
```bash
python3 --version
python3
>>>print("Hello World")
>>>Hello World
>>>exit()
```
```bash
git --version
git clone https://github.com/git/git --depth=1 #Connted through Ethernet.
#Got SSL certificate missing.
#Updated the system clock using:
date -s "2025-09-21 20:11:00"
git clone https://github.com/git/git --depth=1 #Worked this time.
```

## ScreenShots
