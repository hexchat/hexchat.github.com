---
layout: post
title: HexChat and antivirus
tags: [blog]
---

A common issue when we make a new release is anti-virus software on Windows flips out and starts flagging it.
In this post I'll try to discuss some of our release process, how to verify you are safe, and that there is
nothing we can actually do about that.

#### Our release process

HexChat tries to take security of releases seriously and I would like to think does a better job at it
than most small open source projects.

Firstly our main website is hosted on Github Pages over HTTPS only, it is only a landing page and
does not host any files. Our downloads are hosted by me (@tingping) personally on a [DigitialOcean VPS](https://m.do.co/c/4ba63fec1971).
This website is only accessible over HTTPS using modern security practices at [dl.hexchat.net](https://dl.hexchat.net).
Our Windows installer [downloads files at runtime](https://github.com/hexchat/hexchat/blob/master/win32/installer/hexchat.iss.tt)
all over HTTPS only.

So at that point you should have gotten everything securely but we can go a step further to verify this. The source downloads
and the [Flatpak repo](https://dl.tingping.se/flatpak/) for Linux are signed by [my GPG key](https://keys.fedoraproject.org/pks/lookup?op=get&search=0xB3C7CE210DE76DFC).
All Windows installers are built, signed, and uploaded by @tomek. We two are the only people you should trust
any official HexChat download from.

The source to [HexChat](https://github.com/hexchat/hexchat) is of course open but also [our build script and all of
the source to build our Gtk stack](https://github.com/hexchat/gtk-win32) on Windows is open source and can be
[built yourself](http://hexchat.readthedocs.io/en/latest/building.html). If anybody finds anything about this that could be
improved or might be an issue feel free to contact us on IRC.

#### Verifying the installer

1. Download the HexChat installer
2. Run it and you should see this including the Publisher line:

   ![](http://i.imgur.com/CIQ7PnC.png)

3. Click on the publisher name to see more information:

   ![](http://i.imgur.com/DLUU2ya.png)

4. And lastly you can click *View Certificate* to see exact details:

   ![](http://i.imgur.com/FI325dx.png)

5. The exact public key to compare against:

   ```30 82 01 0a 02 82 01 01 00 a4 44 55 27 b5 f1 64 bf 11 09 15 38 aa 5f b2 01 72 06 a2 db 95 79 0f 17 d1 62 29 4c 08 f1 e1 e0 dd 65 da f8 b9 db 1b c5 fa 49 93 e4 9e 3b d9 56 03 cf 1e d8 a4 6a 27 3b 9b 21 50 86 a8 1a 2a c9 3b c5 77 b0 b6 53 ad 81 8a 39 e5 20 bc 5c f9 d4 00 0d e1 d2 47 a0 ca 7b 69 96 61 24 56 1d bd bd 42 37 72 81 27 8e 8c 9a f4 07 84 24 fc b5 a2 51 7f 24 6a 8b 5b 2b 0b fe 79 a8 fa 73 53 c7 f6 d3 ae 6a 08 46 10 37 37 f1 45 80 39 18 86 39 9c 0d 88 ef 57 cc 6c 50 b0 40 4a a2 b1 fb c4 e5 21 45 2b 11 33 69 62 98 5b 8a 57 0c 7d 43 a1 3a 6c e4 e7 95 b4 df 8e 1d c3 cd b4 58 75 62 f5 4a 55 0a 94 05 1f 92 54 31 18 17 08 99 10 0a 88 eb 41 02 2c 25 0b eb 2d b5 e2 86 ac 59 ae f2 d2 4c 3d 7c 43 3d e4 83 00 c0 a5 fb f9 a9 25 cc 1c a6 d8 2b b3 02 55 75 29 cf 28 89 91 91 7e 99 56 2d e1 b7 02 03 01 00 01```

Now that the installer is verified does that mean it is safe? Well the truth is that this is impossible to assert.
You must have impllict trust that @tomek and I are not malicous. There is also a very small chance that
a third party whos software we use is actually malicious but as mentioned above you can verify all software
we use.

#### Why is it flagged?

We don't write your AV software so we don't actually know. There are plenty of assumptions that can be made though;
For one thing IRC has historically been used in a lot of malware and since \[He\]xChat is open source it is plausible some
of that very code was used or they just flag the IRC protocol entirely outside of whitelisted applications.

Another common reason HexChat is flagged is because other users can write arbitrary things in chat that we log. A
tactic some spammers use is to print malicious HTML in chat; This is absolutely harmless to us as we do not parse HTML
or execute JavaScript at all but it will make your AV angry.

#### What can be done?

The only course of action is to whitelist HexChat for now and contact support for your AV.
This happens every release and usually a few weeks after they will add it to the whitelist. You might suggest that
we contact every provider ourselves but this is a task that does not scale up nor is it our problem. Hopefully we
can make you feel a little more confident that it is probably not actually malware though.
