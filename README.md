![HASSIO_TVBOX](https://travis90x.altervista.org/wp-content/uploads/2023/03/TVBOX-Home-Assistant-Armbian-e1678439993545-800x445.jpg)

# Install Home Assistant Supervised with no Architecture Check (no exit on errors)
This installation method is for advanced users only, use at your own risk!

## Instructions for installing Home Assistant Supervised on TV box or Raspberry Pi 5 Debian 12 Bookword
## can be found [here](https://travis90x.altervista.org/home-assistant-supervised-on-armbian-tvbox/)

### Tested on TV Box X96 Mini (SoC ARM Rockchip rk322x armv7l) using qemuarm
with Armbian_23.5.0-trunk.138_Rk322x-box_bookworm_edge_6.3.1.img (Debian 12)

#### Install the Home Assistant Supervised Debian Package:

```bash
wget https://github.com/Travis90x/supervised-installer/releases/latest/download/homeassistant-supervised.deb
sudo apt install ./homeassistant-supervised.deb
```

## Supported Machine types

- generic-x86-64
- odroid-c2
- odroid-c4
- odroid-n2
- odroid-xu
- qemuarm
- qemuarm-64
- qemux86
- qemux86-64
- raspberrypi
- raspberrypi2
- raspberrypi3
- raspberrypi4
- raspberrypi3-64
- raspberrypi4-64
- raspberrypi5-64
- tinker
- khadas-vim3

## Configuration

The default path for our `$DATA_SHARE` is `/usr/share/hassio`.
This path is used to store all home assistant related things.

You can reconfigure this path during installation with

```bash
DATA_SHARE=/my/own/homeassistant dpkg --force-confdef --force-confold -i homeassistant-supervised.deb
```

## Troubleshooting

If something's going wrong, use `journalctl -f` to get your system logs. If you are not familiar with Linux and how you can fix issues, we recommend to use our Home Assistant OS.
