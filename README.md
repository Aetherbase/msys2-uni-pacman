# msys2-uni-pacman
Universal package installer for Msys2 and Arch linux with aur and abs support.
I made this especially for msys2 because support for core and community packages is very less.
I recommend using msys2 over wsl and cygwin because of its native support.

## Installation
just copy the pacuni script to any dir of $PATH 
copying makepkg.conf is optional. It contains various options to optimize building packages on msys2. ***Arch Linux users should NOT use it.Only for msys2***
```
chmod 755 pacuni && cp pacuni /usr/bin && mkdir -p /usr/src/arch
mv /etc/makepkg.conf /etc/makepkg.conf.bak && cp makepkg.conf /etc/ #ONLY for MSYS2
```
## Usage 
For now it just supports installation
It will automatically determine if the package is available from pacman , if not,it will search for PKGBUILD in ABS (core packages/community) and then finally search in aur and will build and install the pkg for u, along with dependencies.
```
pacuni pkg1 pkg2 pkg3 ...
```
## Future development
Iwill try adding more features for flexiblity and reliablity. Users can pull request for more features. Enjoy!!
