++++++
F.A.Q.
++++++

Why use the launcher?
=====================

* Supply of custom fixes (recipe changes, config options, crash fix..)
* Support for additional mods to enhance the gameplay (TabbyChat, VoxelMods, Fastcraft..)
* Always up to date with the server
* Partitial updates (only changed files get updated)
* Custom modpacks

Common Launcher Issues
======================
1. The error below means that you are using an incorrect version of Java. Make sure you look at the table above to make sure you have the right version!

.. code-block:: sh

    The game is running. Please wait.
    Unrecognized option: -p
    Error: Could not create the Java Virtual Machine.
    Error: A fatal exception has occurred. Program will exit.
    Process ended with code: 1
 
2. The error below means you have the wrong JVM arguments for your launcher. Go to options<Java and try only putting in the following ``-Djava.net.preferIPv4Stack=true``. This is fixed in `New` downloads of the launcher.

.. code-block:: sh

   The game is running. Please wait.
   Unrecognized VM option 'UseCMSCompactAtFullCollection'
   Error: Could not create the Java Virtual Machine.
   Error: A fatal exception has occurred. Program will exit.
   Process ended with code: 1


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