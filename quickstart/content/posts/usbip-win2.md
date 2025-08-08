+++
date = '2025-08-08T12:33:43-05:00'
draft = true
title = 'usbip win2'
+++

# usbip-win2

This is a short tutorial written for my mother and sister on how to access the [PE-DESIGN security dongle][10] from your computer. The [PE-DESIGN software][] requires that a particular "card reader & writer" device be connected to your computer before it will open.

I have setup a [software driver][1] that allows one to use a USB device over any network. In this particular case, this means even across the Internet! The **server** and **security dongle** both are physically located in my bedroom.

Your two computers are both *clients* to the server I have setup on my end. This computer is known as `pve3.home` and `pve3-wifi.home` to me.

## Usage
### PE DESIGN Security Dongle

![Screenshot: PE-DESIGN error](/usbip-win2/pe-design_error.jpg)

This is the issue at hand -- **PE Design** requires a *special* USB box to be present before the software will carry on.

#### Attaching this device

![Screenshot: Attaching a device](/usbip-win2/usbip_attached.jpg)

- Attach the device before you are ready to open **PE Design**

#### Detaching this device

- Always be sure to detach this device once you are done using **PE Design**.

- No body else can use the dongle until you *detach* this device; or your computer goes to sleep, whichever comes first.

![Screenshot: Device Already Exported](/usbip-win2/usbip_error.jpg)

- If you see this message, this means one of two things:

a) the security dongle is attached you are ready to go!

b) somebody else has checked out this device and you can check with the other users to see if they are using it.

#### Clients

- jessie
    - `usbip.479831.xyz:62400`
        - `usbip.479831.xyz` is the **server**'s hostname
        - `62400` is the **port** number
![usbip.479831.xyz:62400](/usbip-win2/wusbip_client1.png)

- alice
    - `pve3-wifi.home:3240`
        - `pve3-wifi.home` is the **server**'s hostname
        - `3240` is the **port** number
- ![pve3-wifi.home](/usbip-win2/wusbip_client2.jpg)

### software driver install

The [software][1] should always be managed by me; this means installation and uninstalling the driver is my job. In the scenario where I am unavailable, you may take a look at the driver's [README][99] and decide whether or not you are comfortable following the instructions precisely. The two most important things you must follow are:

- always use the **OSSign** driver release
- always create a [Restore Point][20] before installing or uninstalling this driver!

#### Restrictions

#### Protocol Restrictions

This solution does not allow *concurrent* use of the dongle at the same time, **but** *...*

#### Internet connection

This setup **requires** the Internet connection on both endpoints to be online.
#### Power

This server does not have UPS protection, and therefore, you will lose your connection to this feature  any time my bedroom circuit suffers a power loss.
#### Service Connectivity

[https://uptime.479831.xyz/status/usbip-win2/](https://uptime.479831.xyz/status/usbip-win2)

## Contact Me

JEFFREY CARPENTER
<jeffrey.carp@gmail.com>
[+1 (479) 249-0307](tel:+14792490307)

## Reference Documents

[0]: https://github.com/vadimgrn/usbip-win2
[1]: https://github.com/vadimgrn/usbip-win2/releases
[10]: https://pe-design
[20]: https://support.microsoft.com/en-us/windows/create-a-system-restore-point-77e02e2a-3298-c869-9974-ef5658ea3be9
[99]: https://github.com/vadimgrn/usbip-win2?tab=readme-ov-file#install-usbip
