The WiiPiiDo comes by default deployed with an [Armbian](https://www.armbian.com/) image,
that was customized to fully support all of the WiiPiiDo components.

Through Armbian, the WiiPiiDo can be used either as a desktop-alike computer,
or as a server.
This way, it it possible to use the WiiPiiDo in the following ways:

- [Using the console through the serial port](#connect-through-the-serial-interface)
- [Using the console through SSH](#connect-through-ssh)
- [Using a desktop environment]()

!!! info
    Independently of the method used to use the board, the login credentials are:

    - **username:** pi
    - **password:** wiipiido

## Connect through the Serial Interface

To connect to the console using the serial interface,
<!-- TODO put link to one USB-to-Serial -->
you need to have a USB to Serial connector,
by connecting it from the host PC's USB port to the WiiPiiDo's Serial
connection highlighted in the following image:

![WiiPiiDo Serial Port](img/wiipiido_serial.jpg)

The WiiPiiDo baud rate is set to *115200*, so, once connected
to Linux machine, you can use for example the [picocom](https://linux.die.net/man/8/picocom) program
to open the serial console:

```bash
$ picocom -b 115200 <serial_port>
```

!!! note

    The `<serial_port>` is the port being used by the USB to Serial connector.

    You can check this by, after connecting the connector to the PC, using the command `dmseg`
    and see in which port the device was connected.

    ![Connect FTDI](img/connect_ftdi.png)

    In this example, we can see that a port was connected to the **ttyUSB0** port.
    As such, in this case, the picocom command would be `picocom -b 115200 /dev/ttyUSB0`.

In Windows, [Putty](https://putty.org) can be used for this effect as well.

In this case, make sure that you are using **Serial** as the **Connection type**.
Once the **Serial line** and **Speed** are with the correct values,
you can start the serial connection by clicking in the **Open** button.

![Putty Serial Connection](img/putty_serial.png)


## Connect through SSH

To connect to the WiiPiiDo through SSH you first need to know it's IP address.
This can be found by either using a network scanner program, like [Fing](https://www.fing.com/),
or by configuring the WiiPiiDo to have a static and known IP,
when connected to it using the serial connection or .

When the IP address is known, you can login to the WiiPiiDo, in a Linux machine by using the following command
`$ ssh pi@<wiipiido_ip_address>`.

Alternately, in Windows, you can use once again, for example [Putty](https://putty.org).


## Activate/Deactivate the Desktop Environment

To activate and deactivate the desktop environment that comes by default,
you can simply enable/disable the display manager that is being used,
which in this case is [LightDM](https://wiki.archlinux.org/index.php/LightDM).

To do this, you can run the following commands in the console.

```bash
# Enable the desktop environment
$ systemctl enable lightdm.service
$ systemctl start lightdm.service

# Disable the desktop environment
$ systemctl stop lightdm.service
$ systemctl disable lightdm.service
```

After rebooting the board, the desktop environment will be active/inactive.
