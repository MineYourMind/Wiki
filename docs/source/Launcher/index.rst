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
MyM Launcher on Ubuntu
-----------
This instruction with 6 Steps intends to help setup a Ubuntu Launcher and Icon that you can quickly access without excessive navigating to launch it.

Oracle Java JDK 8 will be installed first.

There will be editing of scripts, extracting an icon from the MyM-Launcher.jar and editing the launcher application file (.desktop)

* File edits will be done with sudo or gksu for graphical editors. nano, gedit, vi or any editor may be used based on familiarity.

* This process is very similar to doing the same with vanilla Minecraft or other Java or "portable" applications that you desire to launch easily.

* Commands using the home userland work directory paths will be instructed.

1. Install Oracle JDK from Command Line
  * ``sudo add-apt-repository ppa:webupd8team/java``
  * ``sudo apt-get update``
  * ``sudo apt-get install oracle-java8-installer``
  Make sure to agree to the terms and wait for it to finish installing

2. Download and create **custom path** to all files
  * Download the MyM Launcher directly from `here <https://mineyourmind.net/#dl_jar>`_
  * *Please manage your own files and folders at your desire*
  * Move or ``copy mv`` or ``cp``. the ``MyM-Launcher.jar`` to a folder designated:
  * *I suggest move (mv)*
  * ``~/Programs/MyM`` is a work directory to store scripts, icons, jar files.
  * ``~`` is the path to your home directory ``/home/user/`` simplified to ``~``

3. Move the file
  * ``mkdir ~/Programs/MyM``
  * ``cd ~/Downloads``
  * ``mv MyM-Launcher.Jar ~/Programs/MyM``

4. Get the built in *Icon graphic* file from within the jar.
  * To get the icon from within the ``MyM-Launcher.jar``. You must open it with archive manager, or mount the archive to access files.
  * Do this by right clicking the .jar file, then select open with **Archive Manager**. It will open and you will see the contents of the Jar File. (See Below)
  
  * ``com``
  * ``junit``
  * ``META-INF``
  * ``org``
  * ``LICENSE.TXT``
  
  * Within the **com** folder, you will find sub folders and the icon. ``/com/skcraft/launcher/bootstrapper_icon.png``
  * **You must right click and open the image first to save it locally.** Because it's within a Java archive, you cannot /copy/paste the image into a folder.
  * Open it with a Image Viewer of your choice. I use Image Viewer built into Ubuntu 16.04.1
  * Once open save it to the ``/MyM`` folder using the Image Viewer Save feature. ``~/Programs/MyM``

5. Create the *bash* script
  * Create and edit a new ``MyM.sh`` bash script.
  * The ``~/Programs/MyM/MyM.sh`` script file will be stored in the ``/MyM`` work directory and ran from the ``MyM Launcher.desktop`` application file when you click it on the Ubuntu launcher as intended.
  * Create ``the MyM.sh`` with sudo or gksu or gksudo with an editor of choice:
  gksu/gksudo allow for gedit or graphical editor to operate under sudo permissions on the graphical desktop.
  Cli/command line - Use a desired editor with sudo.
  * ``gksudo gedit /home/user/Programs/MyM/MyM.sh``
  
  * Copy the following code, and paste it into the sh file:
  * ``#!/bin/bash``
  * ``cd /home/user/Programs/MyM``
  * ``java -jar MyM-Launcher.jar``
  
  * Save the editor

6. Set permissions
  * This makes it executable to run.
  * ``sudo chmod a+x ~/Programs/MyM/MyM.sh``

7. Creating and editing ``MyM Launcher.desktop`` file.
  * Edit the ``MyM Launcher.desktop`` file.
  * The ``~/.local/share/applications/MyM Launcher.desktop`` file will be stored in the user land of a personal user account and will only be reachable by you by using the ubuntu launcher search method.
  * **Mind the case of the letters, and there is a space between MyM and Launcher.desktop**
  * *At the command line:* 
  * ``gksu  gedit ~/.local/share/applications/MyM Launcher.desktop``
  * Copy this into the command line: 
  * `Code <http://hastebin.com/itunoqimev>`_
  * Paste it, save it, and close it.

8. Place the launcher application icon.
  * Open File Manager on the launcher, select **[Computer]** from list and navigate to:
  ``~/.local/share/applications/``
  * Locate your **MyM Launcher** in the folder with the **icon** displayed, and **drag it over to your launcher**.

9. Test and... profit!
  * If all steps are followed properly, launching the MyM-Launcher.jar in **Ubuntu** will work as desired.


Created by: `Meli0 <https://mineyourmind.net/forum/members/meli0.13089/>`_


  







  



  

Known issues
============

Mac OS X
---------

Not required since 4.3 unless the install location of java was modified.

Mac OS X is shipping the java version 6 and even if 7 or 8 is installed it still prefers java 6. Due to this you will need to tell the launcher where to find the newer java version's in order to be able to enjoy the modpacks which require java 7 or newer.

1. Make sure you have Java 7 or 8 installed (Mac only ships with Java 6 by default)
2. Open your system controls and select the java control panel
3. Click on the option that is called "show", "view" or similar (there shouldn't be many)
4. It will show you the installed java version and the path to the location where it is stored
5. Copy this path into the "JVM Path" textbox on the MyMLauncher under "Options.."
6. By default installation of java the path looks like this: (/Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home/bin/java)
7. You should be able to play modpacks that require java 7, now.

-----------

Planned
=======

* bootstrapper for auto-updates
* reuse valid sessions
* bright design (as alternative to the dark one)

Implemented
===========

* new ui design
* search bar
* per modpack icons
* new newspage design
* optional install location
* auto retry failed downloads
* warn about java 6 incompatibility with some modpacks
* custom java installation detection on mac
* improved (auto) java ram settings for 32 bit systems
