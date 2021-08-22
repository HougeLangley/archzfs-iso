# Archiso with zfs

* archzfs repo added
* zfs-dkms instead
* zfs-utils added
* stable linux kernel

## For now have two version ISO:

1. Stable kernel and stable ZFS;
2. Stable kernel and git viersion ZFS.

![zfs-archlinux](https://user-images.githubusercontent.com/1161594/127529134-7044487b-fe96-4775-ad53-38fcd85a5030.png)

![Screenshot_archlinux_2021-08-22_11:12:41](https://user-images.githubusercontent.com/1161594/130341130-d2e29284-e6de-4900-ae22-9a92d3359fac.png)

![Screenshot_archlinux_2021-08-22_11:39:00](https://user-images.githubusercontent.com/1161594/130341182-e29139fb-2c0f-4e48-8abd-6e2c57b537c4.png)

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
