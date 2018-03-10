---
layout: default
title: Downloads
---

## Windows

### Windows 7/8/10

HexChat {{ site.version }} installers: ( [x86]({{ site.dl_url }}/hexchat/HexChat%20{{ site.win_version }}%20x86.exe) / [x64]({{ site.dl_url }}/hexchat/HexChat%20{{ site.win_version }}%20x64.exe) )

Note that the installer automatically downloads other dependencies and may require
rebooting for scripting interfaces to work.

#### Development builds

Latest development versions can be found at: [dl.hexchat.net/hexchat/testing](https://dl.hexchat.net/hexchat/testing)

### Windows 10 S

Windows 10 users can get the latest version on the [Windows Store](ms-windows-store://pdp/?productid=9nrrbgttm4j2).

## Linux
Normally your distribution already has a package though it may be outdated.

### Bundles
Note that these may not fully integrate into your system like traditional packages. They should be portable
across multiple distributions though.

#### Flatpak

This is the officially supported and recommended method to installing on Linux and will always be
up to date. You can find instructions to install Flatpak here: https://flatpak.org/getting.html

{% highlight sh %}
# Stable releases:
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub io.github.Hexchat

# Development releases:
flatpak install --from https://dl.tingping.se/flatpak/hexchat.flatpakref
{% endhighlight %}

#### Snap

{% highlight sh %}
sudo snap install hexchat
{% endhighlight %}

## OS X

There are no longer maintained OSX builds.

## Source
- [Development Version](https://github.com/hexchat/hexchat/archive/master.tar.gz)
- [{{ site.version }}]({{ site.dl_url }}/hexchat/hexchat-{{ site.version }}.tar.xz)
- [Archives]({{ site.dl_url }}/hexchat/)
