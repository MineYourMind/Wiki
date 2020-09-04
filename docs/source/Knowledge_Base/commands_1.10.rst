+++++++++++++
Commands 1.10
+++++++++++++

General
=======
* ``/spawn`` - Teleports you to the spawn point
* ``/sethome [name]`` - Sets your home location and optionally name it
* ``/money`` - Shows the amount of MyMs you own
* ``/pay [player] [amount]`` - Sends money to a player
* ``/baltop`` - Displays the top 5 richest players
* ``/suicide`` - Kills yourself
* ``/stats`` - Shows the time you have spent on all servers
* ``/vote`` - Displays vote links to earn rewards by voting for the server
* ``/ts`` - Shows our TeamSpeak3 IP
* ``/website`` - Shows our website url
* ``/forum`` - Shows our forum url
* ``/premium`` - Shows our shop url

Chat
====
* ``/msg [player] [message]`` - Sends a private message
* ``/r [message]`` - Reply to the last player that sent you a message
* ``/ignore <player>`` - Toggles ignoring of the specified player, disallowing them from sending you messages
* ``/mail send [player] [message]`` -  Sends an offline message
* ``/mail`` - Checks your offline message(s)
* ``/mail clear`` - Clears all your offline message(s)
* ``/party`` - Shows party chat commands
* ``/friend`` - Shows friend commands

Claims
======
* ``/trust [player]`` - Gives the player permissions to build
* ``/untrust [player]`` - Revokes any permissions of the player
* ``/trustlist`` - Lists all trusted players
* ``/abandonclaim`` - Deletes the claim you're standing in
* ``/claimslist`` - Lists your claims

See :ref:`ref-griefprevention` for more information.

Island
======
* ``/island create`` - Creates an island
* ``/island reset`` - Deletes your island and starts a new one
* ``/island setspawn`` - Sets your island's spawn point at your position
* ``/island spawn <username>`` - Teleports you to your island's spawn point (Only use <username> if you are a trusted island member and not the owner)
* ``/island homesetbiome <biometype>`` - Change your island biome type

.. note:: The biome options are ``ocean``, ``swampland``, ``forest``, ``flower_forest``, ``jungle``, ``plains``

Market
======
* ``/market open`` - Opens the buy interface
* ``/market add [price] <amount>`` - Creates a listing for the market. You need to be holding the item you wish to list in your hand.

Tickets
=======
* ``/ticket`` - Shows information regarding ticket creation
* ``/ticket create`` - Creates an empty ticket and displays a link in which to fill in the information

See :ref:`create-ticket` for more information.


.. _patron-commands-110:

Patron
======
* ``/ca`` - Allows to change your cosmetic armor
* ``/claimfarewell [message]`` - Changes the leave message of your claim
* ``/claimgreeting [message]`` - Changes the enter message of your claim
* ``/nick`` - Allows to change the nickname
* ``/hat`` - Sets the current selected block as hat
* ``/patron friendpass [player]`` - Gives the player a friend pass

LegacyTiers
===========
**Tier1:**

* ``/kit <kitname>`` - Shows all kits, or redeems the defined kit
* ``/anvil`` - Opens a portable anvil window only you can use

**Tier2:**

* ``/enderchest`` - Opens your enderchest at will
* ``/workbench`` - Opens a 9x9 crafting window
* ``/et <power>`` - Opens a vanilla enchanting table window (1.10 command only)

**Tier3:**

* ``/back`` - Teleports you back to a previous location
* ``/feed`` - Fills your hunger bar, and saturation
* ``/hat`` - Put the item your holding on your head

 
**Tier4:**

* ``/back`` - Also teleports you back to your death location    (Excludes both Ag's and Sf2; read Tier 3 for more information)
* ``/fly`` - Enables creative fly mode    (Excludes both Ag's and Sf2)
* ``/nick [nickname]`` - Set a nickname
* ``/delnick`` - Deletes your current nickname
* ``/heal`` - Heals yourself
 
**Tier5:**

* ``/god`` - Enables god mode, making you invincible, disabling damage taken (Not including damage that bypasses creative ex. Chaos Guardian)
* ``/thru`` - Moves you through the block(s) you're looking at, right clicking a compass has the same effect
* ``/jump`` - Moves you to the block your cursor is pointing at, right clicking a compass has the same effect

Utility
=======
* ``/cm`` - Manage your chunk loaders
* ``/entitycontrol list-near`` - Get a list of entities in a 3x3 chunk radius
