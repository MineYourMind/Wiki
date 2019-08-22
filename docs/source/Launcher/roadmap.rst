++++++++++++++++
Issues and Plans
++++++++++++++++

Known issues
============

The list of modpacks could not be downloaded
--------------------------------------------

* This happens for a few reasons. Usually, it means your firewall is blocking access to the download servers. To allow the application for your firewall, see the guide below. 
* If allowing it in your firewall did not fix it, it could also be caused when an application forces Java to use IPv6 instead of IPv4. To fix this, please look in your installed programs for a program called ``RelevantKnowledge``. This application is a known malware that alters internet traffic and causes unwanted behaviour. Remove it, and it should fix this issue. If all else fails, see below on how to force java to use IPv4.

`Windows 10 Firewall Guide <https://pureinfotech.com/allow-apps-firewall-windows-10/>`__

**Forcing Java to use IPv4:**

1. Open command prompt (windows start button, type cmd in search)
2. Click the top left of command prompt, click properties, enable quick edit mode
3. Copy this command: ``setx _JAVA_OPTIONS -Djava.net.preferIPv4Stack=true``
4. Right-click on command prompt window to paste it and then hit enter.

Please report any issues on our `forums <https://mineyourmind.net/forums>`__ or through an in-game ticket!

Planned
=======

* Bootstrapper for auto-updates
* Reuse valid sessions
* Bright design (as an alternative to the dark one)

Implemented
===========

* New UI design
* Search bar
* Per modpack icons
* New news page design
* Optional install location
* Auto retry failed downloads
* Warn about Java 6 incompatibility with some modpacks
* Custom Java installation detection on Mac
* Improved (auto) Java RAM settings for 32 bit systems