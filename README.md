# Yocto-Pi

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
     - Set `RM_OLD_IMAGE = "1"` and `INHERIT += "rm_work"`.
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
    sudo apt-get install picocam
  - Used CH340G USB To TTL(Serial) for connecting to pi.
    <img width="572" height="52" alt="Screenshot 2025-09-20 085744" src="https://github.com/user-attachments/assets/95f21292-648f-49e1-8846-019a73b1b3cc" />

> **Note:** I couldn't get the Serial Communication working, So I switched to HDMI using a video-capture card and `OBS Studio` <

    
