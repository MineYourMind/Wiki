+++++++++++++
KnowledgeBase
+++++++++++++

========
Commands
========

General
-------
* ``/spawn`` - Teleports you to the spawn point
* ``/sethome`` - Sets your home location
* ``/pvp`` - Toggle PVP on/off
* ``/ignore &a<player>`` - Show the ignore list or ignore a player
* ``/money`` - Shows your money
* ``/pay [player] [amount]`` - Send money to a player
* ``/money top`` - This displays the top 5 richest players
* ``/suicide`` - Kills yourself
* ``/stats`` - Shows your ontime
* ``/vote`` - Vote for our server and get rewards
* ``/ts`` - Show our TS3 IP
* ``/website`` - Show our website url
* ``/forum`` - Show our forum url
* ``/premium`` - Show our shop url

Chat
----
* ``/msg [player] [message]`` - Sends a private message
* ``/r [message]`` - Reply to the player
* ``/mail send [player] [message]`` -  Send a offline message
* ``/mail read`` - Check your offline messages
* ``/mail clear`` - Remove your messages

Claims
------
See :ref:`ref-griefprevention-tutorial` for more information.

Island
------
* ``/island`` - Opens the GUI
* ``/island restart`` - Deletes your island and start a new one
* ``/island sethome`` - Set your island teleport point
* ``/island home`` - Teleports to your island home point
* ``/island invite [player]`` - Invite a player to join your island
* ``/island trust [player]`` - Same as invite but allows to keep the island for the trusted player
* ``/island untrust [player]`` - Removes the build permission for the player
* ``/island [accept/reject]`` - Accept or reject the invite (Your own Island get deleted)
* ``/island party`` - View your island members
* ``/island leave`` - Leave another player's island
* ``/island kick [player]`` - Remove a player from your island
* ``/island warp [player]`` - Warp to another player's island
* ``/island setwarp`` - Set your island's warp location
* ``/island togglewarp`` - Enable/disable warping to your island
* ``/island ban [player]`` - Ban/unban a player from your island
* ``/island lock`` - Non-group members can't enter your island
* ``/island unlock`` - Allow anyone to enter your island
* ``/island makeleader [player]`` - Makes the player to the owner of the island

Market
------
* ``/market listings`` - Opens the buy interface
* ``/market mail`` - Open your mailbox
* ``/market create [price] <amount>`` - Creates a listing. You need to be holding the item you wish to list in your hand.
* ``/market pricecheck`` - Check the item in your hand's price

Tickets
-------
* ``/ticket`` - Create a new ticket

See :ref:`ref-ticket` for more information.

Premium
-------
**Tier1:**

* ``/kit <kitname>`` - Shows all kits and gives you the kit
* ``/enderchest`` - Open your enderchest from any place
* ``/workbench`` - Open a crafting grid from any place
* ``/is flag [greeting/farewell] [message]`` - Change the leave/enter message of your island

**Tier3:**

* ``/back`` - Teleports you to the latest location
* ``/feed`` - Fills your hunger bar
* ``/hat`` - Sets your item in the hand as hat
* ``/is flag deny-spawn [mob]`` - Denys the specific mob to spawn on your island
 
**Tier4:**

* ``/back`` - Teleports you back to your death location
* ``/fly`` - Enables creative fly mode
* ``/nick [nickname|off]`` - Set a nickname
* ``/heal`` - Heals yourself
 
**Tier5:**

* ``/god`` - Enables god mode to get no damage
* ``/is flag creeper-explosion [deny/allow]`` - Enable/Disable Creeper explosion

----------

.. _ref-griefprevention-tutorial:

========================
GriefPrevention Tutorial
========================
 
.. image:: https://i.imgur.com/9yf2Cf2.png
  :height: 120px!important
  :align:  right
 

Create a claim
--------------

Use your first Chest to create a claim or use a golden shovel and click two corners with it to create your claim. If you use the golden shovel to create a claim then you have to look that the claim is at least 10x10 blocks, else it will not work. Everything in this claim is protected from outsiders.
The glowstone and gold shows you the corners which you can hide with a stick if you right click in the outside of your claim or you click in the inside to show them.
 
Trust a player
--------------

To grant someone the permissions to build in your claim you have to use the command ``/trust [Player]`` during you are in your claim. If you run the command in the outside then the player get trusted in all your claims.
It is also possible to revoke the permissions, for this you have to use ``/untrust [Player]``.
 
Delete a claim
--------------

You can delete one claim or all claims. To delete a claim you have to stand in the claim and use the command ``/abandonclaim``, use it again to confirm it. If you want to delete all your claims you need to use the command ``/abandonallclaims`` and use the command again to confirm it.
  
 
Commands
--------
 
* ``/Trust [Player]`` - Gives the player permissions to build
* ``/TrustList`` - Lists all trusted players
* ``/UnTrust [Player]`` - Revokes any permissions of the player
* ``/AbandonClaim`` - Deletes the claim you're standing in.
* ``/AbandonAllClaims`` - Deletes all of your claims.
* ``/AccessTrust [Player]`` - Gives a player permission to use your buttons, levers...
* ``/ContainerTrust [Player]`` - Gives a player permission to use and open everything.
* ``/PermissionTrust [Player]`` - Grants a player permission to share his permission level with others.
* ``/Untrust All`` - Removes all permissions for all players in your claim.
* ``/SubdivideClaims`` - Switches your shovel to subdivison mode, so you can subdivide your claims.
* ``/BasicClaims`` - Puts your shovel back in basic claim mode.
 
Fakeplayers
-----------
 
* [CoFH]
* [[Forestry]]
* [ComputerCraft]
* [FakeThaumcraftGolem]
* [FakeThaumcraftBore]
* [[BuildCraft]]
* [SFM_Player]


----------


========================
Getting the Crash-Report
========================

If your game crashes and you want to get it solved we require the crash report which get automatically created.


MyM Launcher
------------

1. Open the Launcher
2. Right click on the modpack and click ``View folder``.
3. Open the ``crash-reports`` folder.
4. Paste the content of the latest crash-report on `Pastebin <http://pastebin.com>`_.
5. Click on the ``Submit`` button and copy the web link.
6. Paste the link in the forum thread/webchat/ticket.


FTB Launcher
------------

1. Open the Launcher
2. Select the modpack, click on ``Edit Modpack`` and on ``Open Folder``.
3. Now you are in the ``mods`` folder, go back to the ``minecraft`` folder.
4. Open the ``crash-reports`` folder.
5. Paste the content of the latest crash-report on `Pastebin <http://pastebin.com>`_.
6. Click on the ``Submit`` button and copy the web link.
7. Paste the link in the forum thread/webchat/ticket.


Technic Launcher
----------------

1. Open the Launcher
2. Select the modpack and click on the small `gearwheel <https://i.imgur.com/23B1fW9.png>`_ below the modapck on the right site
3. Now you click on ``OpenFolder`` and open the ``crash-reports`` folder.
4. Paste the content of the latest crash-report on `Pastebin <http://pastebin.com>`_.
5. Click on the ``Submit`` button and copy the web link.
6. Paste the link in the forum thread/webchat/ticket.

ATLauncher
----------

todo


----------

.. _ref-nether-portal:

================================
Multiplex Nether Portal Tutorial
================================
First you need to build a vanilla nether portal. If you are done you have to place a sign below the portal with the word `portal` in the first line. Make sure that the obsidian above the sign has air above it. Now the sign only needs an redstone signal to open a navigation GUI. In the GUI you can select your target destination and unlock other dimensions like End, Twilight Forest etc.
For a demonstration watch `this <https://www.youtube.com/watch?v=BO7RGqFTDzs>`_.


===============================
IRC Introduction and Guidelines
===============================

Introduction
------------

.. warning::
   Avoid frustration and speed up getting to a solution by reading the following guidelines. As things are not like you may be used to.

Unless you are a IRC power user please read up on the following guidelines in order to avoid frustration and get to a solution faster. IRC and its usage is not like a normal chat room. Real life matters of friendliness often delay support and cause frustration.

Guidelines
----------

Below is a list of simple rules helping you to achieve the most out of using general IRC channels

- **Simply ask your question**, there is need to ask if you might ask.. This only delays an answer to your question or help on a matter. *Further busy IRC users tend to answer to quick forward questions but don't respond to "might I ask, anyone around, how is it going.." due to the extra work and being unfriendly than not responding to a question requiring more than a few words.*
- **Ask direct questions and include relevant information.** Increase the possibility of a quick respond by asking questions in a way where simple answers can be made without the need of asking for more details.
- **Keep it short!** No one wants to read a wall of text while being busy, so keep it short but still include all relevant information and allow for a quick answer.
- **Be patient!** Responses can take hours. People in an IRC channel are not there waiting for people to join and chat with them. They might not even be on the computer, be focused on work or playing a game. Give them time to respond and don't wait for an answer. (Do it like them and have IRC open in background, checking from time to time for updates/responses)
- **Tag specific users?** In case you know who to speak to, `tag` him by including the full IRC name in the message, this causes the users IRC client to send out an alert. When the user is active he will be notified about your message. Do not abuse it, or you might be removed from the channel without receiving any help.
- **Be friendly and refrain from acting demanding** No one is obligated to help you, so don't act like they would be. The chance of being ignored raises with your level of demanding and unfriendliness.
- **Crash related issue?** If your issue is related to a client crash, please check out [this post](https://mineyourmind.net/forum/wiki/crash-report/) and include the link to the crash-report in your question. *Posting a massive amount of characters will auto kick you from the IRC channel.*
