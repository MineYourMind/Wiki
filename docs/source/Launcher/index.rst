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
This instruction with 7 Steps intends to help setup a Ubuntu Launcher and Icon that you (Home Ubuntu 16.04.x User)  can quickly access without excessive navigating to launch it.

Summary of Steps involved: 

* Oracle Java JDK 8 will be installed first.

* There will be editing of scripts, extracting an icon from the MyM-Launcher.jar and editing the launcher application file (.desktop)

* File edits will be done with sudo or gksu for graphical editors. nano, gedit, vi or any editor may be used based on familiarity.

* This process is very similar to doing the same with vanilla Minecraft or other Java or "portable" applications that you desire to launch easily.

* Commands using the home userland work directory paths will be instructed.

1. Install Oracle JDK from Command Line 
  * This installs Java 8 for the entire system. 
  * This Java is recommended but other variations of Java will work.
  
  .. code-block:: none
  
    sudo add-apt-repository ppa:webupd8team/java
    sudo apt-get update
    sudo apt-get install oracle-java8-installer
  
  * Make sure to agree to the terms and wait for it to finish installing. This can take some time. 

2. Download and create **custom path** to all files
  * Download The Official free MyM Launcher directly from `here <https://mineyourmind.net/#dl_jar>`_
  * ***Please manage your own files and folders at your desire***
  
  
  * Move or ``copy mv`` or ``cp``. the ``mymlauncher.jar`` to a folder designated
  * *I suggest move (mv)*
  * ``~/Programs/MyM`` is a work directory to store scripts, icons, jar files.
  * ``~`` is the path to your home directory ``/home/user/`` simplified to ``~``

3. Move the file
  .. code-block:: cl
  
    mkdir ~/Programs/MyM
    cd ~/Downloads
    mv mymlauncher.jar ~/Programs/MyM

4. Get the built in *Icon graphic* file from within the jar.
  * This process requires opening and copying the graphic from the ``MyM-Launcher.jar`` - to copy the file you must mount the jar file by right clicking and [Open With] Archive Mounter. once mounted you can browse the .jar file and copy the image. 
  
  * if you accidently use [Open With] Archive Manager, and attempt to copy, an error will be presented to you because you have not mounted the archive. But if you double click the graphic, it will open in an Image Viewer - then you can save it from there. 
  
  .. code-block:: none
  
    com
    junit
    META-INF
    org
    LICENSE.TXT
  
  * Within the **com** folder, you will find sub folders and the icon. ``/com/skcraft/launcher/bootstrapper_icon.png``

  * Once you have the icon,  save it to the work directory in ``~/Programs/MyM``

5. Create the *bash* script
  * Create and edit a new ``MyM.sh`` bash script.
  * The ``~/Programs/MyM/MyM.sh`` script file will be stored in the ``/MyM`` work directory and ran from the ``MyM-Launcher.desktop`` application file when you click it on the Ubuntu launcher as intended.
  
  .. code-block:: cli
  
   gedit /home/user/Programs/MyM/MyM.sh
  
  * Copy the following code, and paste it into the sh file:
  .. code-block:: sh
  
    #!/bin/bash
    cd /home/user/Programs/MyM
    java -jar MyM-Launcher.jar
  
  * Please make edits to accomidate the filename at your time of download. 
  
  * Save the editor

6. Set permissions
  
  * This makes jar/sh files executable to run.
  ``chmod a+x ~/Programs/MyM/MyM.sh``
  ``chmod a+x ~/Programs/MyM/MyM-Launcher.jar``
  
  * The jar, and .sh files are not executable by the user. 
  
  * Alternativly you can use the File application to right click/ Properties then tab Permissions, and check Execute. 

7. Creating and editing ``MyM-Launcher.desktop`` file.
  
  * Edit the ``MyM-Launcher.desktop`` file and allow this user account can use the launcher. 
  
  * The ``~/.local/share/applications/MyM Launcher.desktop`` file will be stored in the user land of a personal user account and will only be reachable by you by using the ubuntu launcher search method.
  
  * **Mind the case of the letters, and there is a dash (-) between MyM and Launcher.desktop** or rename it to desired name. 
  
  * *At the command line:* 
  
  .. code-block:: cl
  
    gedit ~/.local/share/applications/MyM-Launcher.desktop
  
  * Copy this into the editor: 
  
    .. code-block:: cl
    
    [Desktop Entry]
  Name=MyM Launcher
  Comment=Launches MyM-Launcher quickly.
  Exec=~/Programs/MyM/MyM.sh
  Terminal=true
  Type=Application
  StartupNotify=true
  Hidden=false

  Actions=MyMForums;
  Path=~/Programs/MyM
  
  [Desktop Action MyMForums]
  Name=Visit the MyM Forums
  Exec=x-www-browser https://mineyourmind.net/forum/
  Terminal=false

  * Paste it, save it, and close it.
  * if MyM Network decides to change the link to the forum, remember to edit that link as well. 
  2


8. Place the launcher application icon.
  * Open File Manager on the launcher, select **[Computer]** from list and navigate to:
  .. code-block:: none
  
    ~/.local/share/applications/
  
  * Locate your **MyM Launcher** in the folder with the **icon** displayed, and **drag it over to your launcher**.

9. Test and... profit!
  * If all steps are followed properly, launching the MyM-Launcher.jar in **Ubuntu** will work as desired.
  * Right clicking the new Launcher will reveal a direct link to the MYM forums! talk amongst yourselves about how awesome
    MyM Network minecraft is. 

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
