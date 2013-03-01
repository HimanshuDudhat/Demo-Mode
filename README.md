Demo Mode
=========

Free kiosk or demo mode for Android.

Demo Mode is an Android homescreen replacement that lets you deploy devices in
the field without worrying about people being distracted by the other apps or
other features on the phone. A restricted set of apps can easily be placed on
the homescreen and protected by an unlock code.

The default password is `meldemo` and can be changed interactively in the
settings or by editing `res/xml/preferences.xml` in the source. You should
probably change it; the QR code provisioner will copy your password to all
the devices for you so you only need to enter it once.

Provisioning
------------

One device can be configured and its configuration can be shared to provision
multiple devices by way of a QR code. This allows for provisioning in
environments without a network connection and without the need for a central
provisioning server.

Currently, the provisioner copies the following:

* password
* homescreen configuration

Demo Mode and the [ZXing barcode reader][zxing] must first be installed on each
device to use this functionality.

Disclaimer
----------

While Demo Mode makes every attempt to restrict the device, Android is an open
ecosystem and individual devices will be more or less possible to restrict. For
example, HTC's Sense UI has a bug in it that make it possible to get at a
standard homescreen when the device reboots. This is not something that one can
easily workaround, but is also not something that a person using the device
for a short period of time would commonly encounter.

This tool is designed to help steer the focus of the device's usage toward a
single set of applications and is not designed to be an entirely foolproof
lock-down mechanism.

Building
--------

Demo Mode requires [SimpleContentProvider][simplecontentprovider]. A
pre-compiled copy comes with this app for convenience, but one can easily link
it in via source.

License
-------
Android Demo Mode  
Copyright (C) 2012-2013 [MIT Mobile Experience Lab][mel]

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License Version 2
as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

[zxing]: http://code.google.com/p/zxing/
[simplecontentprovider]: https://github.com/mitmel/SimpleContentProvider
[mel]: http://mobile.mit.edu/
