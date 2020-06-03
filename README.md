# Unifi Network Controller Snap

## Install

```
snap install unifi-network-controller
```

The first time it starts up it can take awhile, and as a result it can sometimes time out. But if you give it time and restart it, it should work. This is especially true on a low power device like Raspberry Pi.

I've personally tested this on arm64 and amd64 devices. The app is java so it SHOULD run on other platform is theory.

### Background
I build this snap because installing the Unifi Network controller was extremely frustrating for me. The [directions for installing on Ubuntu/Debian](https://help.ui.com/hc/en-us/articles/220066768-UniFi-How-to-Install-and-Update-via-APT-on-Debian-or-Ubuntu) are long, and there are lots of dependencies. It says that you can install it on Ubuntu 18.04, but it seems like it's targeted at 16.04. Building in a container is also difficult because the controller needs to be on the same LAN as the access points, switches, etc that it's controlling.