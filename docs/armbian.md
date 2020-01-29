

## Activate/Deactivate the Desktop Environment

To activate and deactivate the desktop environment that comes by default,
you can simply enable/disable the display manager that is being used,
which in this case is [LightDM](https://wiki.archlinux.org/index.php/LightDM).

To do this, you can run the following commands in the console.

```bash
# Enable the desktop environment
systemctl enable lightdm.service
systemctl start lightdm.service
```
```bash
# Disable the desktop environment
systemctl stop lightdm.service
systemctl disable lightdm.service
```

After rebooting the board, the desktop environment will be active/inactive.
