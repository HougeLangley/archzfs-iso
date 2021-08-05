# Archiso with zfs

* archzfs repo added
* zfs-dkms instead
* zfs-utils added
* stable linux kernel

![zfs-archlinux](https://user-images.githubusercontent.com/1161594/127529134-7044487b-fe96-4775-ad53-38fcd85a5030.png)

Build image:

```
pacman -S archiso
```

```
mkarchiso -v -w work -o out .
```

Record it on a device:

```
sudo dd if=out/archlinux_zfs-DATE-x86_64.iso of=/dev/sdevice status=progress bs=1M
```
