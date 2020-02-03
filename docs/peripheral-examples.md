# Peripheral Examples

In this section there are examples on how to utilize some of the components the WiiPiiDo has, through the terminal.

<!-- ### 1-Wire -->

<!-- ### ADC -->

<!-- ### Accelerometer -->

<!-- ### GPIO -->

<!-- ### GPS -->

<!-- ### NB-IoT -->

<!-- ### PWM -->

<!-- ### RTCC -->

### Wi-Fi
To connect to a new Wi-Fi AP through the terminal, you can use the terminal interfaces provided by the
[NetworkManager](https://wiki.archlinux.org/index.php/NetworkManager) package,
which comes installed by default in the Armbian image.

This way, we can connect to a new network by using the command `nmcli`, using a console client,
or `nmtui`, using a terminal user interface.
`nmtui` is easy and intuitive to use, so in this example we will have the commands for using `nmcli`,
to serve has a different perspective.

As such, we can first run `nmcli radio`  to check if the Wi-Fi is enabled,
the output should be something like the following:

``` bash
[dedukun@dedu-debian:~] $ nmcli radio
WIFI-HW  WIFI      WWAN-HW  WWAN
enabled  disabled  enabled  enabled
```
