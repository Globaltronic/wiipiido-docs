The WiiPiiDo comes by default deployed with an [Armbian](https://www.armbian.com/) image,
that was customized to fully support all of the WiiPiiDo components.

This image comes


### Login credentials

The default login credentials are:

- **username:** wiipiido
- **password:** wiipiido

## Connect through the serial interface

## Activate/Deactivate the Desktop Environment

To activate and deactivate the desktop environment that comes by default,
you can simply activate/disable the display manager that is being used,
which in this case is [LightDM](https://wiki.archlinux.org/index.php/LightDM).

To do this, you can run the following commands in the terminal.

```bash
# Enable the desktop environment
$ systemctl enable lightdm.service
$ systemctl start lightdm.service

# Enable the desktop environment
$ systemctl stop lightdm.service
$ systemctl disable lightdm.service
```

After rebooting the board, the desktop environment will be enabled/disabled.
