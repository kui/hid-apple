hid-apple
======================

a linux driver fixed for Apple Wireless Keyboard 2011.

"fn" key of Apple Wireless Keyboard 2011 does not work on a driver used on Ubuntu 12.04,
because it's driver is generic-blooth driver.

In terminal:

```sh
$ dmesg | grep bluetooth
[   37.652063] input: SOME_DEVIDE_NAME as /devices/pci0000:00/0000:00:1d.0/usb2/2-1/2-1.8/2-1.8:1.0/bluetooth/hci0/hci0:43/input13
[   37.652131] generic-bluetooth 0005:05AC:0255.0007: input,hidraw4: BLUETOOTH HID v0.50 Keyboard ...
```

[kui/hid-apple][] driver is a fixed hid-apple driver for the above problem.

[kui/hid-apple]: https://github.com/kui/hid-apple "kui/hid-apple · GitHub"

Installation
---------------------

```sh
make
sudo make install
```


Reference
-------------------

* [HOW TO Add Support for KYE, UC-logic, and Waltop Tablets in Ubuntu - Ubuntu Forums](http://ubuntuforums.org/showthread.php?t=1946486)
* <https://launchpadlibrarian.net/94610947/alu2011.patch>
