# Yocto-Pi 🚀

This repository documents my step-by-step **Yocto Project journey**,  
where I build custom Linux images for QEMU (and later Raspberry Pi).  

Each numbered folder contains one stage of the journey, with logs, screenshots,  
and configuration files. This serves as both my learning diary and a resource for others starting with Yocto.

---

## 📚 Stages Completed

1. [Quick Build](01_quick-build/README.md)  
   - Followed the official Yocto Quick Build guide  
   - Built `core-image-sato` and booted it in QEMU.  

2. [Core Image Full Command Line](02_core-image-full-cmdline/README.md)  
   - Built `core-image-full-cmdline` (console-only image)  
   - Booted into Raspberry Pi5 and tested login.  

3. [BBlayers and Packages](03_bblayers-and-packages/README.md)
   - Learnt how do add/remove bblayers using commands.
   - How to add specific recipes to local.conf before bitbaking.
   - Successfully booted to Pi 5 and tested the recipes.

---

## 🔮 Next Planned Stages
- Custom Layer & Recipe  
- Raspberry Pi Target  

---

## 🤝 About Me
I’m a B.Tech (Electronics & Computer Engineering) student exploring **Embedded Linux**  
and the **Yocto Project** for building custom Linux distributions.
