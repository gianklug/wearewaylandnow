+++
title = 'Discord'
tags = ['X.org','PTT','Screen sharing']
+++

**AFK handling**

You might've noticed that you aren't getting any mobile notifications while Discord running under Wayland is open. This is due to the AFK detection not working because Discord doesn't know about your cursor outside of its window. The following BetterDiscord plugin fixes this, by adding an inactivity timeout:  
[https://github.com/Colonial-Dev/WayAFK](https://github.com/Colonial-Dev/WayAFK)

**Screen Sharing**

As Discord doesn't support screen sharing via pipewire, you're usually better off by using the browser version or [WebCord](https://github.com/SpacingBat3/WebCord). There is another workaround, namely `xwaylandvideobridge`. This creates an Xorg window, mirroring your pipewire screen sharing for Discord to pick it up:  
[https://invent.kde.org/system/xwaylandvideobridge](https://invent.kde.org/system/xwaylandvideobridge) ([AUR package](https://archlinux.org/packages/extra/x86_64/xwaylandvideobridge/))

**Push to talk**

Similar to the other issues, discord can't access your keyboard while the app window isn't focused. There is a helper script that redirects the direct key events to Discord, allowing push-to-talk to work:  
[https://github.com/Rush/wayland-push-to-talk-fix](https://github.com/Rush/wayland-push-to-talk-fix)

**Wayland-native alternative**

If you do not need push-to-talk, you can also use [Vesktop](https://github.com/Vencord/Vesktop), which has native Wayland support. Screen sharing also works out of the box.
