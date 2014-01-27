---
layout: post
title: Announcement
tags: [announcement]
---

Say Goodbye to XChat-WDK, Say Hello to HexChat!

As some of you have already noticed, we've changed the name. Why was it required? Why now? Why this name? What's next? Let me address these.

XChat-WDK started in 2010. Back then XChat itself was alive and kickin', so XChat-WDK was Windows-only. It was pointless to support Linux, as it was already supported by XChat.

A lot of things have changed since then. XChat is now practically abandoned. There's only one active committer left, and he's the maintainer of the Perl interface. In the meanwhile XChat-WDK evolved and instead of just fixing Windows-specific bugs it introduced new features as well. Then it started to make more and more sense to support multiple platforms, not just Windows. Sometime ago I put some effort into making XChat-WDK compile on \*nix so now we can say, XChat-WDK is multiplatform.

Our original goal was to merge XChat-WDK with XChat, but our previous contact person is simply lost (we haven't heard of them since new year's day), and our recent attempt to reach Zed has failed, too. We waited for the xchat.org domain to expire, which was due in June, but the domain was eventually renewed. Apparently Zed wants to keep XChat, so we had no other choice but to create a new project.

But remember, WDK stands for the Windows Driver Kit, so it doesn't make any sense to use a Windows-specific name for a multiplatform application. The change was necessary.

What does HexChat mean? Well, basically, nothing spectacular, it's just a name which tries to sound good. HexChat is pronounced and written almost identically as the predecessor, XChat, so it seemed like a good name for a new beginning. Anyway, it means "six" with Greek origins, and Hex is also used in programming. That's about it.

What does the future hold? Well, we have a lot of work to do! We have to rebrand this thing, introduce some sane release management process (probably starting at something like 2.9.0) so that \*nix packagers can actually package HexChat releases for their distros. The repo needs to be cleaned properly. A migration to GitHub is also possible to happen. And if everything goes well, we might as well merge with XChat-Azure, too.

That means one project for Windows, \*nix and Mac, folks! Don't expect these things to happen really fast though. We're doing our best to bring all these to you as soon as possible. In the meanwhile, just keep chatting. Thanks for your understanding and have a nice day :)