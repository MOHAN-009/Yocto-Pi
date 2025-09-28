# Yocto-Variables

# Basic Variables

*PN_PV_PR.bb* - Pattern for recipe name.

- To read any variable:
```bash
bitbake -e <RECIPE_NAME> | grep ^<VARIABLE_NAME>
```

- PN : Package name
```bash
bitbake -e <recipe_name> | grep ^PN=
```

- PV : Package version (Default `"1.0"`)
```bash
bitbake -e <recipe_name> | grep ^PV=
```

- PR : Package revision (Default `"r0"`)
```bash
bitbake -e <recipe_name> | grep ^PR=
```

- WORKDIR : recipe location, it's located in the TMPDIR structure (*PN/PV-PR* - display format)
```bash
bitbake -e <recipe_name> | grep ^WORKDIR=
```

- S : Source location of build directory where unpacked recipe source code resides (*WORKDIR/PN-PV*)
```bash
bitbake -e <recipe_name> | grep ^S=
```

- B : Build directory - Same as *Source*
```bash
bitbake -e <recipe_name> | grep ^B=
```

- D : Destination directory. It is the location in the Build Directory where components are installed by the do_install task. This location defaults to WORKDIR/image.
```bash
bitbake -e <recipe_name> | grep ^D=
```