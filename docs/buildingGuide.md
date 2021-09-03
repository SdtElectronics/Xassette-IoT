# Build From Scratch
## Dependencies
### For Debian users:
```
$ sudo apt-get update 
$ sudo apt-get install git g++ make libncurses5-dev subversion libssl-dev gawk libxml-parser-perl unzip wget python xz-utils vim zlibc zlib1g zlib1g-dev openjdk-8-jdk build-essential ccache gettext xsltproc
```
### Extra operations for Debian 64bit:
```
$ sudo dpkg --add-architecture i386
$ sudo apt-get update
$ sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386
```
### For ArchLinux users:
```
$ vim /etc/pacman.conf 
    # Uncomment these:
    [multilib]
    Include = /etc/pacman.d/mirrorlist

$ sudo pacman -S base-devel subversion asciidoc b43-fwcutter bash bc bin86 boost binutils bzip2 cdrkit fastjar flex gawk gettext git gtk2 intltool jdk7-openjdk libusb libxslt ncurses openssl patch perl python2 rsync ruby sdcc sharutils unzip util-linux wget zlib gcc make perl-extutils-makemaker findutils libstdc++5 lib32-libstdc++5 gperf
```

## U-Boot
U-Boot from widora almost works out of the box, the only thing we need to do is to modify the size of DDR RAM.

### 1. Grab the code:
```
$ git clone https://github.com/widora/u-boot-mt7688.git
```
### 2. Extract toolchain:
```
$ cd u-boot-mt7688
$ sudo tar xvfj buildroot-gcc342.tar.bz2 -C /opt/
```
### Install openjdk:
```
$ sudo apt install openjdk-8-jdk
or $ sudo pacman -S jdk8-openjdk
```

### 3. Build
```
$ make clean;make
```
The output file would be 'uboot.bin'

## OpenWrt
* TODO