# simple-switch-cmake
switch simple devkitpro project that initialise the window with glfw and glad

## Requirements

Install or configure the pacman from <a href="https://devkitpro.org/wiki/devkitPro_pacman">devkitpro website</a> and Use the following command to install the necessary packages:

``` sh
sudo dkp-pacman -S switch-dev switch-cmake switch-tools switch-glfw switch-mesa switch-glad switch-glm 
```

for arch folks: 

``` sh
sudo pacman -S switch-dev switch-cmake switch-tools switch-glfw switch-mesa switch-glad switch-glm 
```

then, update the PATH enviroment variable as follows: 

``` sh
#DEVKITPRO tools
export PATH=$PATH:/opt/devkitpro/tools/bin/
#DEVKITPRO binaries
export PATH=$PATH:/opt/devkitpro/devkitA64/bin/
```

add this command into .bashrc or .zshrc to make change persistent 

## Building

we need to use the <a href="https://github.com/devkitPro/catnip">catnip</a> command and it can be found at ```/opt/devkitpro/tools/bin/catnip``` in linux and is part of 'switch-tools' package

``` sh
catnip -T switch
```

This command will generate a build folder. Inside that folder, you will find the main.release directory, and the generated .nro file will be named simp.nro.

use that nro file to play the games on the switch! :D
