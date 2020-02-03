The WiiPiiDo has support for [Yocto](https://www.yoctoproject.org/)
by use of an Bitbake BSP Layer, which can be found at <a class="fa fa-github" href="https://github.com/Globaltronic/meta-wiipiido"></a>.

!!! warning
    The Yocto support is still in it's early states, if you are not familiar with Yocto,
    or want something more stable, we recommend you to use the [Armbian image](getting-started.md).

## Building from Source

Follow the usual steps to setup OpenEmbedded and bitbake,
after sourcing **oe-init-build-env** add the WiiPiiDo BSP Layer with the `bitbake-layers` command.

```bash
cd poky
git clone https://github.com/Globaltronic/meta-wiipiido.git
source oe-init-build-env
bitbake-layers add-layer ../meta-wiipiido
```

Then compile a new image with the WiiPiiDo as the new target:

```bash
MACHINE=wiipiido bitbake core-image-base
```
