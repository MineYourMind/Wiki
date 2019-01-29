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


MyM Launcher on Ubuntu
----------------------
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

2. Download, creation of directory and moving of files

Download The Official free MyM Launcher directly from `here <https://mineyourmind.net/>`_ by scrolling down and clicking the button at the bottom that says ``Mac + Linux``

Now we need to run a few commands to get the directory made, and the launcher moved to the proper folder

  .. code-block:: cl
  
    sudo mkdir ~/Programs/MyM
    cd ~/Downloads
    mv MyM-Launcher.jar ~/Programs/MyM

3. Getting the Icon from within the jar.

  * Right click the `MyM-Launcher.jar` and choose `Archive Manager`
  * Then navigate to `/com/skcraft/launcher/` and click the `bootstrapper_icon.png` and then click `Extract`
  * Once you have the icon,  save it to the work directory in ``~/Programs/MyM``

4. Create the *bash* script

Create and edit a new ``MyM.sh`` shell script.

The ``MyM.sh`` script file will be stored in the ``~/Programs/MyM`` work directory and executed from the ``MyM-Launcher.desktop`` application file when you run it.

Run the following command to make the shell script
  .. code-block:: cl
  
   gedit /home/user/Programs/MyM/MyM.sh
  
Copy the following code, and paste it into the script file

  .. code-block:: sh

    #!/bin/bash
	cd ~/Programs/MyM
	java -jar MyM-Launcher.jar

Save the file and close the editor. Please make edits to accomidate the filename at your time of download!

5. Set permissions
  
Run the following commands to make the Shell Script and the Launcher Jar executable. This will allow us to run them later on to get the launcher working.

  .. code-block:: cl

  	chmod a+x ~/Programs/MyM/MyM.sh
  	chmod a+x ~/Programs/MyM/MyM-Launcher.jar

Alternatively, you can use the File Explorer to right click the file and choose Properties->Permissions, and check Execute. 

6. Creating and editing a ``MyM-Launcher.desktop`` file
  
We will be making a file in ``~/.local/share/applications`` called ``MyM-Launcher.desktop``. This file will only be usable by your current user, and will need to be repeated for other users who wish to have an independent launcher install.
  
**Mind the case of the letters and name format!**
  
At the command line run the following command to create the file
  
  .. code-block:: cl
  
    gedit ~/.local/share/applications/MyM-Launcher.desktop
  
Copy this into the editor
  
  .. code-block:: cl
  
	[Desktop Entry]
	Name=MyM Launcher
	Comment=Launches MyM-Launcher quickly.
	Exec=/home/<USER>/Programs/MyM/MyM.sh
	Terminal=true
	Type=Application
	Icon=/home/<USER>/Programs/MyM/bootstrapper_icon.png
	StartupNotify=true
	Hidden=false

Change *<USER>* to your username, save it, and close the window.

7. Final Checkup.

In the ``~/Programs/MyM/`` folder, you should have the following items: ``MyM-Launcher.jar``, ``MyM.sh`` and ``bootstrapper_icon.png``

If those items are present, you can safely copy the ``MyM-Launcher.desktop`` from ``~/.local/share/applications`` to your desktop using the following commands

  .. code-block:: cl

    cd ~/.local/share/applications
    cp MyM-Launcher.desktop ~/Desktop

and run it from the desktop to enjoy our launcher!

If you still have issues after following this guide, please double check all steps. If there are still issues, please report it to us on the `forums <https://mineyourmind.net/forums>`_ or through an ingame ticket!

Created by: `Meli0 <https://mineyourmind.net/forum/members/meli0.13089/>`_

Updated 01/29/2019 by Column01

Known issues
============

None!

Please report any issues on our `forums <https://mineyourmind.net/forums>`_ or through an ingame ticket!

Planned
=======

* Bootstrapper for auto-updates
* Reuse valid sessions
* Bright design (as alternative to the dark one)

Implemented
===========

* New UI design
* Search bar
* Per modpack icons
* New newspage design
* Optional install location
* Auto retry failed downloads
* Warn about Java 6 incompatibility with some modpacks
* Custom Java installation detection on Mac
* Improved (auto) Java RAM settings for 32 bit systems