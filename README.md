# starcom_serial_driver

Startech usb serial converter driver.

This is a Linux kernel patch which adds a device ID to 
the ti_usb_3410_5052 kernel driver, for a starcom usb-to-serial 
converter I have lying around (device id: 14b0:3410)

## Note for Gentoo users

You'll have to install sys-kernel/linux-firmware with the 'unknown-license' use flag enabled
in order to pull the required firmware files:

    * ti_3410.fw
    * ti_usb-v14b0-p3410.fw

This use flag has been masked by default, so you'll have to unmask it by adding the line below
to a file in `/etc/portage/profile/package.use.mask`

```
sys-kernel/linux-firmware -unknown-license
```

