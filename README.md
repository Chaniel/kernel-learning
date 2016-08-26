# kernel learning
### kernel compile
0. dependencies
    yum groupinstall "Development Tools" "Development Libraries" -y
1. generate .config file
    make menuconfig
2. compile
    make
3. install modules
    make modules_install
4. install kernel
    make install

** time make install **
can count time

### kernel development
    check lab03 dir

### Linux booting sequence
POST --> DISK MBR 446B(bootloader(grub)) --> kernel(vmlinuz) --> (initrd(initramfs.img,init)) --> (ROOTFS)/sbin/init(/etc/inittab, /etc/fstab, /etc/rc.d/) 





