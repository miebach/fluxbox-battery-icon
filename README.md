fluxbox-battery-icon
====================

Fluxbox battery icon perl script by OTPABA

Licence: No licence found. Free to use. "Feel free to modify".

Author: OTPABA - http://forums.fedoraforum.org/member.php?u=193747

See http://forums.fedoraforum.org/showpost.php?s=ec087e478399a39882347f0fd6c77c39&p=1567472&postcount=8

Oignally copied from: http://forums.fedoraforum.org/attachment.php?attachmentid=22927&d=1333531555


Publishing message from OTPABA:

----

Hi all,

since Gnome v2 is not available any more by default, and my desktop must have 10 static workspaces (hard to change habits after 12 years) I switched to Fluxbox and obviously felt lack for some features. After my laptop died few times due to battery discharge I just spent few minutes to code a primitive but helpful status-bar battery icon. Works for me...

It is written in perl. It does not use native ACPI support. I simply used /usr/bin/acpi output instead (make sure you install acpi package before: yum install acpi). Icon will show you 100%, 75%, 50%, 25% changes. It turns full-red and starts blinking when battery is bellow 10%. When hovered you can see pop-up label like:

"Battery 0: Charging, 11%, 03:15:21 until charged"

It gets updated every 30 seconds. I used embedded / base64 encoded icon images to avoid dependencies. In my case I installed it under ~/scripts/baterryIcon.pl with 0755 (-rwxr-xr-x) permissions. It gets started by ~/.fluxbox/startup with a line:

~/scripts/baterryIcon.pl &

I'll be glad if you try it. I'll be happy if you like it  Feel free to modify it if you need.

Generally it does not try to write anything to your system at all, so it should be safe to run, but please use it on your own risk and be aware of the following:

CAUTIONS:

- never tested on systems others than Fedora 15;
- never tested on a desktop computer without battery;
- never tested on a laptop with more than one battery;
- never tested on a different Window Manager than Fluxbox v1.3.2

Attached Files
	batteryIcon_v1.pl.gz (6.1 KB, 97 views)

Last edited by OTPABA; 4th April 2012 at 12:01 PM.

----





