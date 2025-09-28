# Yocto-Creating and Adding Layers

# Creating Layer

- Contains information/recipes to build packages.
- Initialized env:
```bash
source oe-init-build-env ../builds/pi
```
- Checked existing layers in `local.conf`
```bash
bitbake-layers show-layers
```
- Priority of Layers
    - If there are 2 identical/same packages in 2 different layers, the layer with the highest priority will execute the recipe.

- Created a custom layer(___ In pocky folder ___):
```bash
bitbake-layers create-layer meta-myproject
```
    - A new layer will have 4 things in it:
        1. conf
        2. COPYING.MIT
        3. README
        4. recipes-example

# Adding Layer

- Added layer to bblayers.conf file:
```bash
bitbake-layers add-layer ../../poky/meta-myproject
```
- Ran the example_0.1.bb in `meta-myproject/recipes-example/example` using:
```bash
bitbake example
```
