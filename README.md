Linuxdroid:Boot
===========
[![Join the chat at https://gitter.im/linuxdroid/linuxdroid](https://badges.gitter.im/linuxdroid/linuxdroid.svg)](https://gitter.im/linuxdroid/linuxdroid)

A [Linuxdroid](https://linuxdroid.app) add-on app to run programs at boot.

- [Linuxdroid:Boot on Google Play](https://play.google.com/store/apps/details?id=com.linuxdroid.boot)
- [Linuxdroid:Boot on F-Droid](https://f-droid.org/packages/com.linuxdroid.boot)

When developing (or packaging), note that this app needs to be signed with the same key as the main Linuxdroid app in order to have the permission to execute scripts.

License
=======
Released under [the GPLv3 license](https://www.gnu.org/licenses/gpl.html).

How to use
==========
1. Install the Linuxdroid:Boot app.
2. Start the Linuxdroid:Boot app once by clicking on its launcher icon. This allows the app to be run at boot.
3. Create the `~/.linuxdroid/boot/` directory.
4. Put scripts you want to execute inside the `~/.linuxdroid/boot/` directory. If there are multiple files, they will be executed in a sorted order.
5. Note that you may want to run `linuxdroid-wake-lock` as first thing if you want to ensure that the device is prevented from sleeping.

Example: To start an sshd server and prevent the device from sleeping at boot, create the following file at `~/.linuxdroid/boot/start-sshd`:

```sh
linuxdroid-wake-lock
sshd
```
