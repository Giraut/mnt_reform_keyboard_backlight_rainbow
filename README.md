# MNT Reform keyboard backlight rainbow
### Version 0.0.1

A small program and systemd service to create a rainbow animation with the backlight LEDs on a MNT Reform laptop.

![MNT hotkey shutdown - Bezel foam pads](images/mnt_reform_rainbow_keyboard_backlight.jpg)



## Installation

### Installing the pre-built .deb package

See [https://github.com/Giraut/ppa](https://github.com/Giraut/ppa) to add the PPA repository to your APT sources.

```
sudo apt install mnt-reform-keyboard-backlight-rainbow
```

### Manual installation

```
sudo apt install python3-setproctitle
sudo install -m 755 ./mnt_reform_keyboard_backlight_rainbow.py /usr/local/bin
sudo install -m 644 ./mnt_reform_keyboard_backlight_rainbow.service /lib/systemd/system
```

### Starting the service

```
sudo systemctl enable --now mnt_reform_keyboard_backlight_rainbow.service
```


### Customization

By default, the `mnt_reform_keyboard_backlight_rainbow.service` systemd service file launches `mnt_reform_keyboard_backlight_rainbow.py` with a 50% backlight intensity and a 2-second refresh delay. Edit the parameters in the service file to your liking, then restart the service.
