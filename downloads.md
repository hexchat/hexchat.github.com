---
layout: default
title: Downloads
---

## Windows 7/8/10
**HexChat {{ site.version }}** ( [x86]({{ site.dl_url }}/hexchat/HexChat%20{{ site.win_version }}%20x86.exe) / [x64]({{ site.dl_url }}/hexchat/HexChat%20{{ site.win_version }}%20x64.exe) )

#### Extra components

##### Note that the installer downloads these automatically and only portable-mode users must manually get these. Also ensure that any Python/Perl installations are installed for all users and added to PATH (this may require rebooting).

Visual C++ 2015 Redistributable ( [x86]({{ site.dl_url }}/misc/vcredist_2015_x86.exe) / [x64]({{ site.dl_url }}/misc/vcredist_2015_x64.exe) )

Dictionaries for spell checking (only needed on Windows 7) ( [r2]({{ site.dl_url }}/hexchat/HexChat%20Spelling%20Dictionaries%20r2.exe) )

Python 2.7.12 for scripts ( [x86](https://www.python.org/ftp/python/2.7.12/python-2.7.12.msi) /
[x64](https://www.python.org/ftp/python/2.7.12/python-2.7.12.amd64.msi) )

Python 3.5.2 for scripts ( [x86](https://www.python.org/ftp/python/3.5.2/python-3.5.2.exe) /
[x64](https://www.python.org/ftp/python/3.5.2/python-3.5.2-amd64.exe) )

Perl 5.20.0 for scripts ( [x86]({{ site.dl_url }}/misc/perl/Perl%205.20.0%20x86.msi) / [x64]({{ site.dl_url }}/misc/perl/Perl%205.20.0%20x64.msi) )

#### Development builds

Latest development versions can be found at: [dl.hexchat.net/hexchat/testing](https://dl.hexchat.net/hexchat/testing)

## Linux
Normally your distribution already has a package though it may be outdated.

### Ubuntu (Mint)
Note these are community maintained repositories.

- [OverCoder's PPA](https://launchpad.net/~overcoder/+archive/ubuntu/hexchat) (Latest stable)
- [Glebihan's PPA](https://launchpad.net/~gwendal-lebihan-dev/+archive/hexchat-stable) (Direct port of Debian's packages)

### Bundles
Note that these may not fully integrate into your system like traditional packages. They should be portable
across multiple distributions though.

#### Flatpak

{% highlight sh %}
flatpak install --from https://dl.tingping.se/flatpak/hexchat.flatpakref
{% endhighlight %}

#### Snap

{% highlight sh %}
sudo snap install hexchat
{% endhighlight %}

## OS X

You can find builds from third party distributors such as [Homebrew](http://brew.sh/) in the [homebrew-gui](https://github.com/Homebrew/homebrew-gui) repository.

## Source
- [Development Version](https://github.com/hexchat/hexchat/archive/master.tar.gz)
- [{{ site.version }}]({{ site.dl_url }}/hexchat/hexchat-{{ site.version }}.tar.xz)
- [Archives]({{ site.dl_url }}/hexchat/)
