# Linux Kernel Learning

## Kernel Compile

0. dependencies
```
yum groupinstall "Development Tools" "Development Libraries" -y
```
1. generate .config file. 
```
make menuconfig
```
2. compile  
```
make
```
3. install modules. 
```
make modules_install
```
4. install kernel. 
```
make install
```
count installation time
```
time make install
```

## Kernel Development
```
    check lab03 dir
```
## Linux Booting Sequence
```
POST --> DISK MBR 446B(bootloader(grub)) --> kernel(vmlinuz) --> (initrd(initramfs.img,init)) --> (ROOTFS)/sbin/init(/etc/inittab, /etc/fstab, /etc/rc.d/) 
```
## Kernel Related Commands
```
lsmod
insmod
modinfo
aliases
vermagic
modprobe
dmesg
```
## Kernel File Location
```
kernel: 
    /boot/vmlinuz
    /boot/initrd
kernel modules:
    /lib/modules/`uname -r`
```



