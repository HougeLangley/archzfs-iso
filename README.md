# Archiso with zfs

* archzfs repo added
* zfs-dkms instead
* zfs-utils added
* stable linux kernel

## For now have two version ISO:

1. Stable kernel and stable ZFS;
2. Stable kernel and git viersion ZFS.

![zfs-archlinux](https://user-images.githubusercontent.com/1161594/127529134-7044487b-fe96-4775-ad53-38fcd85a5030.png)


## Archinstall for regular user:

```
archinstall
```

## Build image:

```
pacman -S archiso
```

```
mkarchiso -v -w work -o out .
```

## Download ISO and Record it on a device:

```
sudo dd if=out/archlinux_zfs-DATE-x86_64.iso of=/dev/sdevice status=progress bs=1M
```
