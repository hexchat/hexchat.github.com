---
layout: default
title: Shareware background
---

##Shareware background

The Official Windows build of XChat is Shareware, and after 30 days, a one time fee of $19.99 is required. This page will hopefully help you understand how this relates to the GPL, and why it was done.

XChat is primarily the project of one man, Peter Železný a.k.a. zed. He has been the primary contributor to XChat since he started the project. XChat was initially developed as a Unix/Linux GTK application, but after a while, there became a demand for XChat to work on Windows. The underlying problem was that there are fundamental differences to the way Windows and X11 handle widget drawing. To get around this issue, Peter customized aspects of the GTK+ for Windows project to strip out many of the features that XChat didn't use (for a smaller binary) and to integrate the appearance and behavior of XChat better into a Microsoft Windows Environment.

The process for doing this was tedious compared to the X11 version, and the time was not otherwise compensated. So with the release of XChat 2.4.0 on August 23, 2004, zed moved the Windows build to a shareware model to compensate him for the time involved in integrating XChat with Microsoft Windows.

Anyone is free to compile XChat for Windows if they want, however there are some complications to this. There are several people who have, and some of those have released their builds for others to use. This is completely legal, and some would argue in the spirit of the GPL. If you are interested in having a free alternative to the official build, you can check out the unofficial builds.

###Features Specific to Official Build

There are a few features that are specific to the official build which are not in the source code. Some of these are due to the nature of them being MS Windows specific needs, others are because of feasibility on Linux.

####Graphical Smilies

The official version includes the ability to include graphical smilies and icons in the main text area. As the code for inline graphics has not been released, it is not possible to see if the code would have worked on POSIX systems or not. It should be possible to include graphics for all versions of XChat with a proper patch, however this has not been done. While SilvereX does claim to support emoticons and the Eye Candy theme, not all of the support is included.

####DCC Server

mIRC introduced an addition to the IRC protocol with the /dccserver command, which allowed sends to go from the "server" to the client, but have the client initiate the communication. The receiver would then get the information, rather than having the sender push the information. By doing this, the responsibility for having more open ports fell on the receiver. The port normally specified for this was Port 59, which is one of the ports restricted by POSIX systems to privileged users. Because it is a bad idea to run normal applications as privileged users (for security and exploit purposes), it does not make sense to include this feature which primarily makes use of port 59. There are, however, patches available if building XChat in an environment where the user is privileged, such as other Windows machines. See DCC Server for more information.

All versions of XChat include a /dcc psend command which will send a file using passive mode, which is what /dccserver was setup to do, however it does not require the recipient to have a specific open port, however it does require the recipient to have more flexibility in terms of the firewall.

####Integration with the Desktop

XChat includes support for native file handling dialogs on Windows, rather than using the GTK version. Because it also uses a static version of GTK (using MiniGTK), zed is able to better integrate XChat with the Windows environment. Some of the unofficial builds use MiniGTK as well, but this is a feature that is not included with the base source code (as MiniGTK is pointless outside of a Windows environment).

###Accused violations of copyright

After this move to shareware, there were many accusations of copyright infringement. Some of these accusations have more merit than others. There had been accusations that a shareware model was incompatible with the GPL if any libraries were linked to. XChat however uses LGPL libraries, which do not have restrictions as to what applications can use them.

There have been patches accepted from third party developers (as in, not from Zed), and so many argued that if no licensing agreement had accompanied the patch, then the patch should be assumed to be under the GPL. This would mean that zed would not control the license of the patch, and could therefore not dual license the code contained in the patch. Because of this, it was offered that any code that a developer did not want included with XChat anymore would be removed and replaced with a new-from-scratch version written by zed.

Although some contend this was not enough to only remove if an author didn't complain (instead of removing all code unless the author explicitly approves), the controversy has been around since 2004. If any author would have had an issue, their code would have already been removed.
And the GPL

It is important to note that XChat still releases the source code under the GPL, so anyone is free to build XChat on any platform they so desire. There are those who do, and some release the builds they have created. These builds are completely legal and do not violate any copyright law (that is known). You can find out more about these alternate builds on the unofficial builds page.

XChat itself now is dual licensed. Contributions to XChat are accepted both as GPL and as assigned to zed, so that the code may be included with the official win32 build. Anyone may modify and distribute XChat in anyway they desire as long as it follows the GPL.

For more info, refer to the forum thread, [About Windows release licensing](http://forum.xchat.org/viewtopic.php?t=533).
