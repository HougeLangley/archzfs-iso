# Archiso with zfs

* archzfs repo added
* zfs-dkms-git added
* zfs-utils-git added
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
## 中文说明 ##

1. Archlinux 和 Gentoo 一直是很多朋友很少接触的 Linux 发行版，都说他们滚动更新，容易出问题，其实，机器是诚实的，出问题的往往是人自己；
2. 那么为了方便大家学习和使用 Archlinux 和 Gentoo，并且方便使用 ZFS 文件系统，这次更新带来的是全新的功能：
  - 可以启动 xfce4 桌面环境，安装更加友好；
  - 自带 Firefox, Telegram, IRC 工具，方便与社区沟通；
  - 大家安装都会把错误或者疑问用手机拍照，别拍了直男、直女们，用 Flameshot 截图吧，自带 Flameshot 截图工具。
  - 其他网络工具（详见下图）。

![Screenshot_archlinux_2022-06-08_23:46:32](https://user-images.githubusercontent.com/1161594/172663643-1cb09286-6934-48b3-be87-f79ac26ccfc7.png)

![Screenshot_archlinux_2022-06-08_23:46:45](https://user-images.githubusercontent.com/1161594/172663927-8a2921a4-6e17-4cb6-a9a0-ab9dc3fd79d9.png)

![Screenshot_archlinux_2022-06-08_23:47:07](https://user-images.githubusercontent.com/1161594/172663979-8dddcf10-090b-486f-85b9-246051ee5bd6.png)

![Screenshot_archlinux_2022-06-08_23:47:27](https://user-images.githubusercontent.com/1161594/172664021-79bdee84-36ca-45fc-907e-711f29c6716d.png)

![Screenshot_archlinux_2022-06-08_23:47:41](https://user-images.githubusercontent.com/1161594/172664053-6c1efd44-b60d-436a-a653-4aa04e0fcb8f.png)

![Screenshot_archlinux_2022-06-08_23:48:38](https://user-images.githubusercontent.com/1161594/172664317-c3a5f7a6-a0fa-4da5-9509-3c9defe79791.png)

## 安装愉快 ##
