# Yocto-Quick-Build

This repository documents my learning journey with the **Yocto Project**.  
The first step was completing the official [Quick Build Guide](https://docs.yoctoproject.org/5.0.12/brief-yoctoprojectqs/index.html).

## 🛠️ Steps Followed
1. Cloned `poky` repository, branch `scarthgap`.
2. Set up environment with `oe-init-build-env ../builds/QuickBuild/`.
3. Ran `bitbake core-image-sato`.
4. Booted the image in **QEMU** with `runqemu qemux86-64`.

## 📂 Outputs
- Successfully built **core-image-sato** (~few hours build).
- Booted into a graphical environment inside QEMU.

  <img width="1531" height="428" alt="Screenshot 2025-09-15 110801" src="https://github.com/user-attachments/assets/00e1f5d6-1fd4-4862-ac36-44580b5579c1" />
  <img width="1276" height="833" alt="Screenshot 2025-09-15 111230" src="https://github.com/user-attachments/assets/e040d8ed-7b2e-4d30-89b7-cb6d71ed9a69" />
  <img width="1396" height="289" alt="Screenshot 2025-09-15 111329" src="https://github.com/user-attachments/assets/9bff607a-6a17-4423-8808-528817333669" />

## 🔮 Next Steps
- Creating a custom layer (`meta-myproject`).
- Writing a simple BitBake recipe.
- Target hardware (Raspberry Pi).

