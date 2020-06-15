# nx-udev

This package installs an udev rule to allow communication via usb with the Nintendo Switch without root access. It does that by changing the permissions (mode) to 666 (rw-rw-rw-).

After installing you may need to replug your device.

# Installing

## Via Package

### Arch Linux

It's available in the [AUR](https://aur.archlinux.org/packages/nx-udev/), so you can install it using makepkg:

```bash
git clone https://aur.archlinux.org/nx-udev.git
cd nx-udev
makepkg -si
```

Or using [yay](https://github.com/Jguer/yay) (or any other AUR helper):

```bash
yay -S nx-udev
```

### Debian, Ubuntu, or any other distro that has `apt`

I've generated a debian package in the [releases](https://github.com/pheki/nx-udev/releases), so you can just install it with `dpkg -i`:

```bash
# Download the debian package
wget https://github.com/pheki/nx-udev/releases/latest/download/nx-udev_latest_all.deb
# Install it
sudo dpkg -i nx-udev_latest_all.deb
```

## Manually

To install manually, just copy `60-nx.rules` and `60-nx-rcm.rules` to `/etc/udev/rules.d/`:

```bash
# Download the repository
git clone https://github.com/pheki/nx-udev.git && cd nx-udev
cp *.rules /etc/udev/rules.d/
```
