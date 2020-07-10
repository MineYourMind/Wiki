.. _ref-worlddownloader:

+++++++++++++++++++++++++++++++
How to use MyM World Downloader
+++++++++++++++++++++++++++++++

.. warning:: 
	Some items in inventories (such as drives in a drive bay) may not download correctly! To insure the highest chance of success, place them in your inventory prior to adding any claims or chunks! 

	Do NOT put them inside of backpacks or any portable storage!

To start off you are going to need the client side version of the mod. You can download it at `this link <http://mym.li/wd>`_ and place it into your ``mods`` folder. Once you do that, restart the game so it can be loaded.

Next you are going to need to add the areas you want and then download them. There are two options for this: Using claims and using radius. Using the radius mode you can download a maximum of 10 chunks around you. The claims mode will add your claim you stand in. You can see how to use either method below.

How to: Using Claims
====================

1. Add your claims to world downloader by running the command ``/wd add claim`` while standing in your claims (works for trusted members too). 

* If you have multiple claims, repeat this for all your claims before moving on to step 2.

2. Once you have added the claims, you can run the command ``/wd dl <downloadName>`` to download the selected claims. This will make a new single player world called ``world`` for you to continue on in single player!


How to: Using Radius
====================

1. Add a radius around you to world downloader by running the command ``/wd add radius <number>`` while standing in the desired area. 
	Note: You can only download the area if it has been claimed by you, or you are trusted in the claim.

* The number is the amount of chunks around you that you want to download. So if you want to download a 4x4 chunk area, put 2 in as that will download the a 4x4 area. Repeat this for all the areas you want to save before moving on to step 2.

2. Once you have added a radius, you can run the command ``/wd dl <downloadName>`` to download the selected area. This will make a new single player world called ``world`` for you to continue on in single player!


I did that, but it didn't make a singleplayer world for me. What do I do!?
==========================================================================

Well you are going to need to make it manually using what it downloaded. Here is what it should download minus a few pack specific folders i've left out:

* playerdata (folder)
* region (folder)
* level.dat

In order to play, you will need to make your own version of the world in single player. Here's how:

1. Go to the singleplayer tab in Minecraft and click "Create New World". Name it something you will remember such as ``MyM Singleplayer`` and make sure it's set to survival with the default world generation options!

2. Once the world generates and you log in and can move, exit out of the world back to the menu.

3. Open up the saves folder for minecraft. If you are using the MyM Launcher and used the default installation directory on windows, this is located at: ``AppData/roaming/.mineyourmind/instances/<instance name>/minecraft/saves``. A shortcut to get here is to open the MyM launcher, right click the pack you are playing and select ``View Folder`` and then go to the ``saves`` folder.

.. note:: 
	Other launchers have similar methods of getting to where it's installed. A quick search around will probably show you how (whether on google or just around the launcher's options)

4. Navigate to the folder named what ever you named the world in Step 1, and copy all the files from the world download there. This will ask you if you want to replace them, make sure to click yes to all of the dialog items! If you don't, some parts will not replace properly.

5. Go back to the main menu of Minecraft, then back to Singleplayer and load the world. This should put you where you were when you downloaded the server and you should have all your stuff you saved! Keep in mind, things like homes will **not** transfer so you may want to write coordinates down for key areas while on the server so you can get back to them in singleplayer.

.. note:: 
	If you still have issues downloading the world or setting it up, please make a ticket using ``/ticket create``
