++++++++
Launcher
++++++++

Why?
====

* Supply of custom fixes (recipe changes, config options, crash fix..)
* Support for additional mods to enhance the gameplay (TabbyChat, VoxelMods, Fastcraft..)
* Always up to date with the server
* Partitial updates (only changed files get updated)
* Custom modpacks

-----------

F.A.Q.
======

How to change the save location
-------------------------------

1. Create a new ``text document``.
2. Include the following code in to the text document:

.. code-block:: none

   SET sPath=%appdata%
   SET AppData=[Location]
   MyM-Launcher.exe
   SETAppdata=%sPath%
   
3. Change [Location] to your custom directory (For example: ``D:\Program Files (x86)\MyMLauncher``).
4. Save the document as ``MyM-Launcher.bat`` in the same directory as the ``MyM-Launcher.exe``.
5. Run the ``MyM-Launcher.bat`` to download and start the modpacks.

-----------

REI Minimap migration
---------------------
These are the steps to migrate the REI's waypoints from FTB Launcher to the MYM Launcher.

1. Open a new window and navigate to your FTB Install Folder

   * You can find the folder by starting the FTB Launcher and pressing options.

2. From the FTB Install folder navigate to [FTB Install Folder]\Monster\minecraft\mods\rei_minimap.
3. In another window, navigate to %AppData%\.mineyourmind\instances\MyM-FTB-Monster\minecraft\mods\rei_minimap

   * You should be able to copy this entire path to your navigation bar.

4. Copy all the .points files from `[FTB Install Folder]\Monster\minecraft\mods\rei_minimap to %AppData%\.mineyourmind\instances\MyM-FTB-Monster\minecraft\mods\rei_minimap`.
5. You might have to rename some files depending on what method you use to connect to the servers

   * If you have been connecting to the lobby and would like to use direct connect on the MYM Launcher, rename your files to have the prefix "monster-new.mineyourmind.net" ``monster.mineyourmind.net.DIM0.points`` **->** ``monster-new.mineyourmind.net.DIM0.points``
   * Other Examples: ``monster-new.mym.li.DIM0.points`` **->** ``monster-new.mineyourmind.net.DIM0.points``

by `slyder5649 <https://mineyourmind.net/forum/threads/reis-migration-to-mym-launcher-win7.1101/>`_


-----------

Known issues
============

Mac OS X
---------

Mac OS X is shipping the java version 6 and even if 7 or 8 is installed it still prefers java 6. Due to this you will need to tell the launcher where to find the newer java version's in order to be able to enjoy the modpacks which require java 7 or newer.

1. Make sure you have Java 7 or 8 installed (Mac only ships with Java 6 by default)
2. Open your system controls and select the java control panel
3. Click on the option that is called "show", "view" or similar (there shouldn't be many)
4. It will show you the installed java version and the path to the location where it is stored
5. Copy this path into the "JVM Path" textbox on the MyMLauncher under "Options.."
6. By default installation of java the path looks like this: (/Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home/bin/java)
7. You should be to play modpacks that require java 7, now.

-----------

Planned
=======

* optional install location
* per modpack icons
* new ui design
* auto retry failed downloads
* reuse valid sessions
* new newspage design
* bootstrapper for auto-updates
* warn about java 6 incompatibility with some modpacks