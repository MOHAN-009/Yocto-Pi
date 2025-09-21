# Yocto-Command-Line

## 🛠️ Project Setup
  1. Initialised environment `source oe-init-build-env`.
  2. Created a directory at the poky level `../../sources`.
  3. Made changes to local.conf:
     - Changed machine to `raspberrypi5`.
     - Changed source path
       ```bash
       SOURCES = "/home/yocto/yocto/sources"
       DL_DIR ?= "${SOURCES}/downloads"
       SSTATE_DIR ?= "${SOURCES}/sstate-cache"
       TMPDIR = "${SOURCES}/tmp"
     - Set `RM_OLD_IMAGE = "1"`(Removes old image before building new image) and `INHERIT += "rm_work"`(Removes unnessaray files from tmp/work/.. to save space).
   4. Built image using - `bibake core-image-full-cmdline`

## 📂 Output
  - Successfully built `core-image-full-cmdline`
  - Image file created at
    ```bash
    sources/tmp/deploy/images/raspberrypi5/
  - Extracted archive file - `core-image-full-cmdline-raspberrypi5.rootfs.wic.bz2` to get `core-image-full-cmdline-raspberrypi5.rootfs.wic` flashable image.
  - Flashed onto a microSD card using **balena-Etcher**.
  - Installed Picocom
    ```bash
    sudo apt-get install picocom
  - Used CH340G USB To TTL(Serial) for connecting to pi.
  <img width="572" height="52" alt="Screenshot 2025-09-20 085744" src="https://github.com/user-attachments/assets/95f21292-648f-49e1-8846-019a73b1b3cc" />
  <img width="471" height="497" alt="Screenshot 2025-09-20 090430" src="https://github.com/user-attachments/assets/9d0b62fd-6a04-44b9-8f12-c0375f3dd495" />


> **Note:** I couldn't get the Serial Communication working, so I switched to HDMI using a video-capture card and `OBS Studio` to view it on my laptop.
  - Logged in using `root`.
  - Ran basic commands:
    ```bash
    uname -r
    uname -a
    lsblk
    ls -l
    pwd
    free -h
    mkdir test
  <img width="625" height="243" alt="Screenshot 2025-09-20 102940" src="https://github.com/user-attachments/assets/6fc6ada1-06c7-4c71-9c01-2df7f07cc64d" />
  <img width="546" height="154" alt="Screenshot 2025-09-20 104011" src="https://github.com/user-attachments/assets/2c75eb61-2a08-4bd7-80ec-541a9ae5e3cd" />





    
