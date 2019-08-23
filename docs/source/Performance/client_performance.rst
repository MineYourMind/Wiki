++++++++++++++++++++++++++
How to increase Client FPS
++++++++++++++++++++++++++

Basic Minecraft
===============

To increase your FPS on many of our modpacks, firstly you will want to open your favorite modpack and go to options.
From there you will need to go to the options tab on the menu.
From there you will want to go to Video settings and do the following:

Set graphics to FAST.

Set View Bobbing to OFF.

Set Clouds to OFF.

Set Particles to MINIMAL.

Set Render Distance to 6 OR BELOW.

Set Smooth Lighting to OFF.

Set V-Sync to OFF.

Make sure you have no resource packs on.

Other ways to increase your FPS include downloading performance enhancers such as Fastcraft which is on most MYM modpacks or even Optifine which will be listed below.

For information regarding how to install these performance mods, please consult the Knowledge Database on installing mods to your launcher

Fastcraft
---------

To install Fastcraft, simply download it at this link here and follow the above instructions: https://www.curseforge.com/minecraft/mc-mods/fastcraft/files

BetterFPS
---------

Algorithm: See what works for you, you can leave this to default if you want
Set Preallocate Memory to Off

Set Fog to FAST

Set Beacon Beam to FAST

Set Fast Beacon to ON

Optifine
--------

Set Dynamic FOV to OFF

Set Use VBOs to ON

**In details:**

Set Trees to FAST

Set Sky to OFF

Set Sun & Moon to OFF

Set Fog to OFF

Set Translucent Blocks to FAST

Set Dropped Items to FAST

Set Vignette to FAST

Set Swamp Colors to OFF

Set Cloud Height to OFF

Set Rain & Snow to FAST

Set Stars to OFF

Set Show Capes to OFF

Set Held Item Tooltips, Entity Shadows, and Smooth Biomes to OFF

**in animations:**

Click "All Off"

**in quality:**

Set Antialiasing and Anisotropic Filtering to OFF

Set Custom Fonts to OFF

Set Connected Textures to OFF

Set Custom Sky, Emissive Textures, Random Entities, Custom Colors, Custom Items, and Custom GUIs to OFF

**in performance:**

Set Fast Render to ON (set to off if this causes issues)

Set Chunk Updates to 1

Set Smooth World to ON

Set Fast Math to ON

Mod specific:
=============

Agricraft
---------

Agricraft sprinklers and water channels can cause huge client/FPS lag. Their particles can be turned off in the mods config. Still, even without the water particles, these sprinklers can be the cause of huge FPS and even TPS lags. Try using as few of them as posible.

Immersive Engineering
---------------------

Immersive Engineering Waterwheels and Windmills have moving parts which can cause client fps issues when looked at if there are too many of them within your field of view.

Item Pipes
----------

Item ducts that aren't opaque from Thermal Expansion and Buildcraft pipes can dramatically reduce your fps as they both show items moving through the pipes. These tile entities can drastically lower your fps, if you are using the clear item ducts from Thermal Expansion. If possible try to use the opaque ones as they are better for your fps and don't show the items moving through the pipes but work at the same transfer rate.

As for Buildcraft, try using pipes from other mods which don't show the items. These days most mods work with just about any machine. If your setup requires BC pipes for whatever reason, try using as few of them as possible. You can also just use BC pipes as entry and exit point of your piping system and then switch to opaque Thermal Expansion ducts, as they will interconnect.



Increasing total amount of ram
==============================

While Minecraft itself needs no more ram than what is allocated by default, modded minecraft can need anywhere from 2 GB minimum to even 6 GB minimum.

Installing 64 bit java
----------------------

Before you set your total memory to an amount larger than 2^32 bits (Or 4 GB), you will need to install 64 bit java.

First, navigate to https://www.java.com/en/download/manual.jsp and select the 64 bit version of java that you need.

Download the file, and make sure that it is installed.

You should be ready for the next steps in increasing the total amount of RAM, but if you run into any issues, you may need to either restart or check to see what went wrong.
..note::
Make sure to set your memory to **no more than half** of your computer's total RAM. This should also not be any more than 6 GB or 6,192 MB unless you are using HD texture packs as you may notice slowdowns as java is unable to dump excess memory.

MyM Launcher
------------

To increase the amount of RAM that is on the MYM launcher, first launch the program and click options.

You will see a screen that says:

General Java Minecraft Proxy Advanced

Click Java, and set the amounts to:

For minimum memory, you can set this to exactly one GB less than your maximum memory, but you can set it to even less if you wish.

For maximum memory, you can set this to no more than half your total RAM or 6 GB as mentioned in the note.

For PermGen you can either set it to 256 for 32 bit and 512 for 64 bit.

Twitch Launcher
---------------

Increasing the amount of memory on the Twitch Launcher needs a few more steps than normal.

First, launch the program and then make sure that you are logged in.

Next, look at the top right where your profile is and click on it (this should open up a menu)

Then click on Settings and navigate to "Minecraft"

Scroll down until you see "Allocated Memory" and drag the slider to the right/left until the allocated memory is no more than half your total RAM or 6 GB taking the note into consideration.

AT Launcher
-----------

To increase the amount of RAM that is on the Technic Launcher, launch the program and click "Settings"

Navigate to the Java/Minecraft tab and set the values to:

For initial memory, you can leave this at the initial value of 512 but you can set it higher if you wish.

For maximum memory, you can set this to no more than half your total RAM or 6 GB as mentioned in the note.

For PermGen you can either set it to 256 for 32 bit and 512 for 64 bit.

Technic Launcher
----------------

To increase the amount of RAM that is on the Technic Launcher, launch the program and click "Launcher Options"

Navigate to the tab called "Java Settings" and set the memory to no more than  of your computer's total RAM.

To make sure that you are using 64 bit java, check in the java version at the top if it says "64-Bit"



Now just test to see if it allocated that memory, launch the pack in question and when you are in-game press F3 and look for something like "Total Memory Usage: x MB used out of (What you put in maximum memory)"

If so, you have successfully increased the amount of memory you have.
