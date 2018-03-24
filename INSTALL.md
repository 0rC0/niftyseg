# Compile and Install on Debian Stretch

DISCLAIMER:
This procedure worked on my computer, I cannot assure it works (or even it is safe) on another one, please use it if you know what are you doing.

```
sudo apt-get install build-essential cmake-gui libeigen3-dev doxygen
cd $nifty_reg_src_dir
mkdir build
cd build
cmake ..
cmake-gui ..
```
press Configure, then
* BUILD_TYPE Release
* Adjust (if needed INSTALL_PREFIX)
press Configure, then Generate, then close the cmake-gui and:
```
make -j`nproc`
make install # or eventually sudo make install
```
