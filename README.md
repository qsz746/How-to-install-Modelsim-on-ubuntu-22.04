# Install Modelsim on a Ubuntu 22.04 Jelly fish

Tested on Apirl 23rd 2024

Reference:
 
 https://pcotret.github.io/modelsim-ubuntu/ <br>

 https://stackoverflow.com/questions/73895565/e-package-lib32gcc1-has-no-installation-candidate 
 

## Solution:
```
wget http://download.altera.com/akdlm/software/acdsinst/13.1/162/ib_installers/ModelSimSetup-13.1.0.162.run
chmod +x ModelSimSetup-13.1.0.162.run
```
 <br>
 
### However, the free version of Modelsim Altera Edition is 32-bit only. We need to install some dependencies:

```
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install build-essential
sudo apt-get install gcc-multilib g++-multilib lib32z1 lib32stdc++6 lib32gcc-s1 expat:i386 fontconfig:i386 libfreetype6:i386 libexpat1:i386 libc6:i386 libgtk-3-0:i386 libcanberra0:i386 libpng16-16:i386 libice6:i386 libsm6:i386 libncurses5:i386 zlib1g:i386 libx11-6:i386 libxau6:i386 libxdmcp6:i386 libxext6:i386 libxft2:i386 libxrender1:i386 libxt6:i386 libxtst6:i386
```

 <br>
 

### Download the ModelSim - Intel FPGA edition installer (both packages) from the Intel homepage.
```
https://www.intel.com/content/www/us/en/software-kit/750666/modelsim-intel-fpgas-standard-edition-software-version-20-1-1.html
```
![image](https://github.com/qsz746/How-to-install-modelsim-on-ubuntu-22.04/assets/55030187/43d48986-380c-43df-8071-ce592747979f)

 <br>

### Make the installer executable

```
chmod +x ModelSimSetup-20.1.1.720-linux.run
```

 <br>

### Run the installer and install ModelSim:
```
./ModelSimSetup-20.1.1.720-linux.run
```

 <br>

### How to open modelsim:
```
./intelFPGA/20.1/modelsim_ase/bin/vsim
```
