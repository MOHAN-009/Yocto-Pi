# Yocto-BBlayers&Packages

## BBlayers

- Checked for existing layers.
```bash
bitbake-layers show-layers
```
<img width="854" height="140" alt="Screenshot 2025-09-21 181815" src="https://github.com/user-attachments/assets/8b0d81ad-6fd1-4410-af8a-0186e4597f8c" />

- Removed a layer.
```bash
bitbake-layers remove-layer meta-raspberrypi/
```
- Re-added the removed layer.
```bash
bitbake-layers add-layer meta-raspberrypi/
```
<img width="853" height="340" alt="Screenshot 2025-09-21 181949" src="https://github.com/user-attachments/assets/d3718763-be1f-416f-a07e-d37aea700fc1" />


## Packages

- Initialised environment.
```bash
source oe-init-build-env ../builds/pi
```
- Checked the recipes.
```bash
bitbake-layers show-recipes #Showed everything 🫠
```
- Checked only the recipes I wanted to pre-install with the image.
```bash
bitbake-layers show-recipes python3 git
```
<img width="1444" height="160" alt="Screenshot 2025-09-21 185438" src="https://github.com/user-attachments/assets/431f9957-6e66-40f3-ab73-2cff570c6e83" />

- Made sure the meta layer is present in `bblayers.conf`.
- Edited local.conf file:
```bash
IMAGE_INSTALL:append = " python3 git"
```
- Built Image to include the new packages `python3` and `git`.
<img width="1433" height="441" alt="Screenshot 2025-09-21 192518" src="https://github.com/user-attachments/assets/54c5b50a-d436-4b3a-8497-7524921ce9b6" />

- Checked if they were added using:
```bash
bitbake -e core-image-full-cmdline | grep "^IMAGE_INSTALL="
oe-pkgdata-util list-pkgs | egrep "git|python3"
#Forgot to take a screenshot :(
```
- Flashed the image onto Pi 5 and booted it successfully.
<img width="1020" height="563" alt="Screenshot 2025-09-21 193454" src="https://github.com/user-attachments/assets/b24646be-8cb6-46b1-a6ee-5a63668a528f" />

- Checked if the packages were installed.
```bash
python3 --version
python3
>>>print("Hello World")
Hello World
>>>exit()
```
<img width="451" height="123" alt="Screenshot 2025-09-21 193755" src="https://github.com/user-attachments/assets/e8b48340-82d5-4e24-a1bd-b77abf0fa0ab" />

```bash
git --version
git clone https://github.com/git/git --depth=1 #Connted through Ethernet.
#Got SSL certificate missing.
#Updated the system clock using:
date -s "2025-09-21 20:11:00"
git clone https://github.com/git/git --depth=1 #Worked this time.
```
<img width="683" height="214" alt="Screenshot 2025-09-21 201225" src="https://github.com/user-attachments/assets/2efbc0df-caf6-42e6-9789-ec1d87789003" />

