# Debian Preseeded Autoinstaller

This package will produce a Debian installer ISO that is fully unattended.

Edit `preseed.txt` to taste, then run `make`. Copy `autoinstall.iso` to your VM provisioning system or burn it to a CD/DVD then boot.

On Debian the following are required:

    sudo apt-get install curl make fuse genisoimage rsync

fuseiso required, and must be fetched+installed manually on current debian:
    
    http://ftp.us.debian.org/debian/pool/main/f/fuseiso/fuseiso_20070708-3_amd64.deb


On any OpenSolaris descendent (SmartOS, OmniOS, Oracle Solaris) the following are required:

* curl
* GNU make
* mkisofs
* rsync

Override parameters using standard `make` variables.

### Examples

Build for i386.

    make ARCH=i386

Build a specific version

    make DEBIAN_VERSION=7.1.0
