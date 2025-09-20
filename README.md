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
    
