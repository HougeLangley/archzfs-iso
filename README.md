# Arch Linux ZFS XFCE Live ISO

> A pre-configured Arch Linux Live ISO with ZFS support and XFCE desktop environment.

![Release](https://img.shields.io/github/v/release/HougeLangley/archzfs-iso)
![License](https://img.shields.io/github/license/HougeLangley/archzfs-iso)

## Features

- **ZFS Support**: `zfs-utils-git` and `zfs-dkms-git` pre-installed
- **XFCE Desktop**: Full-featured desktop environment with modern applications
- **Boot Support**: BIOS/UEFI with Syslinux and systemd-boot
- **Chinese Support**: FCITX5 input method, Noto CJK fonts, WenQuanYi fonts
- **Network Tools**: NetworkManager, OpenVPN, v2raya, Xray, and more
- **System Tools**: btop, htop, tmux, neovim, flameshot, testdisk, smartmontools
- **Disk Tools**: Clonezilla, fsarchiver, partclone, gpart, ddrescue
- **Archinstall**: Built-in automated installation script

## Download

Latest ISO available at [GitHub Releases](https://github.com/HougeLangley/archzfs-iso/releases).

> **Note**: Due to GitHub's 2GB file limit, ISO files larger than 2GB are split into parts.
> 
> To merge: `cat archlinux_zfs_xfce_live-*.iso.part.* > archlinux_zfs_xfce_live-*.iso`

## Quick Start

### Write to USB

```bash
# Merge split parts (if applicable)
cat archlinux_zfs_xfce_live-*.iso.part.* > archlinux_zfs_xfce_live.iso

# Write to USB device
sudo dd if=archlinux_zfs_xfce_live-*.iso of=/dev/sdX bs=1M status=progress

# Or use GNOME Disks, Etcher, or Rufus
```

### Boot

- **BIOS**: Select "Arch Linux ZFS XFCE Live" from Syslinux menu
- **UEFI**: Select EFI Boot from firmware menu

### Install

Once booted, use the built-in `archinstall` script:

```bash
archinstall
```

Or follow the [official Arch Linux installation guide](https://wiki.archlinux.org/title/Archinstall).

## Build from Source

### Prerequisites

```bash
# On Arch Linux
sudo pacman -S archiso squashfs-tools
```

### Build ISO

```bash
# Clone repository
git clone https://github.com/HougeLangley/archzfs-iso.git
cd archzfs-iso

# Build ISO
mkarchiso -v -w work -o out .

# Output: out/archlinux_zfs_xfce_live-YYYY.MM.DD-x86_64.iso
```

### Customize

Edit `packages.x86_64` to add/remove packages:

```bash
# Add package
echo "your-package" >> packages.x86_64

# Rebuild ISO
mkarchiso -v -w work -o out .
```

## Configuration Files

| File | Description |
|------|-------------|
| `packages.x86_64` | Package list for x86_64 architecture |
| `profiledef.sh` | ISO profile definition (name, version, boot options) |
| `pacman.conf` | Pacman configuration with archzfs repository |
| `syslinux/` | Syslinux bootloader configuration |
| `airootfs/` | Custom root filesystem modifications |
| `efiboot/` | EFI boot files |

## Included Packages

### Desktop & Applications
- XFCE4 desktop environment
- Firefox, Telegram, irssi, weechat
- Alacritty, Kitty terminal emulators
- Flameshot screenshot tool

### System & Disk
- ZFS on Linux (DKMS)
- btrfs-progs, xfsprogs, jfsutils
- LVM2, mdadm, dmraid
- Clonezilla, fsarchiver

### Network
- NetworkManager with applet
- OpenVPN, vpnc, rp-pppoe
- v2raya, Xray, proxychains-ng
- nmap, tcpdump, ndisc6

### Developer Tools
- Git, Neovim, Tmux
- Python, pip, xray
- Nix package manager

### Utilities
- btop, htop, ncdu
- testdisk, gpart, smartmontools
- mc (Midnight Commander)
- zsh with grml configuration

## 中文说明

这是一个为 Arch Linux 学习者准备的预配置 Live ISO：

### 特点

1. **ZFS 文件系统支持**：内置最新 ZFS 驱动，可直接创建和挂载 ZFS 池
2. **友好的桌面环境**：XFCE4 + 常用应用，开箱即用
3. **中文支持**：拼音输入法、中文字体齐全
4. **网络工具**：包含 v2raya、Xray 等网络工具
5. **系统工具**：Clonezilla、testdisk 等磁盘工具
6. **截图工具**：Flameshot，方便记录问题和分享

### 适用场景

- 学习 Arch Linux 安装和配置
- 使用 ZFS 文件系统的实验环境
- 系统救援和数据恢复
- 日常使用的轻量级 Linux

### 安装建议

1. 使用 `archinstall` 进行自动化安装
2. 选择 ZFS 作为根文件系统
3. 配置好镜像源后再进行系统更新

## Release Notes

See [GitHub Releases](https://github.com/HougeLangley/archzfs-iso/releases) for changelog.

## Contributing

1. Fork the repository
2. Modify `packages.x86_64` or configuration files
3. Test build with `mkarchiso`
4. Submit a pull request

## License

MIT License - See [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Arch Linux](https://archlinux.org/) - The base distribution
- [ArchISO](https://wiki.archlinux.org/title/Archiso) - ISO building tools
- [archzfs](https://github.com/archzfs/archzfs) - ZFS repository

---

**Happy installing! 🚀**
