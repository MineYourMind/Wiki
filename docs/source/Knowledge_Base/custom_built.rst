++++++++++++
Custom Built
++++++++++++

Plugins (bukkit)
================

ProtectEx
---------
ProtectEx is an anti-griefing plugin designed to protect Claims and Restricted Areas from unauthorized use, building, and use of certain tools and inventory items.

ItemRestrict
------------
Restricts items from being used in certain worlds or at all

Backup
------
Automaticly backs up the server to ensure your work is safe

ChunkManager
------------
Our custom built chunk plugin use /cm introduction to find out more

Claim/Island Deleter
--------------------
Automaticly deletes claim/island after 2 weeks of a player being inactive

Redis Chat
----------


Stats
-----
Keeps track of your play time and other useful stats use /stats me to see them

Announcer
---------
Allows staff to make global announcements when needed

Vote
----
Allows players to get tokens and reminds them to vote regularly 

Random Teleport
---------------
Using /rt you can teleport to a random location on the map

Ranks
-----
Ranks show how long you have been playing on MyM servers

ForumFeed
---------
Displays information from your linked fourm account

MultiBlockLimit
---------------
This reduces lag by limiting the amount of blocks you can place in a multiblock structure

Forum/Ticket InterOp
--------------------
Allows staff to see tickets and other useful information

Custom Third Party Forks
------------------------

- Grief Prevention
- zPermissions
- Pex
- Vault
- Console Nuke
- Thread Lock
- WorldBorder
- MinecraftRKit
- Lag Meter
- Item Restrict
- Forge Perms
- Command Helper
- Accept Rules
- Ban Manager
- UUID Provider

Misc
----

- Local Wither Sound
- Keep Exp
- Safe Login
- Chunk Monitor

Mods (forge)
============

Kit
---
allows for kits to give you items in game

World Downloader
----------------
Allows a player to download there claim to single player and test or continue to play there mainly uses when a server is shutting down

EntityControl
-------------
Allows staff to control/limit mob spawning

Chunk Deleter
-------------


MyM-Tweaks
----------
Applys several tweaks to allow all servers to operator correctly

MyMKit
------


ModPatches
----------
Allows staff to fix gameplay breaking mod issues

Custom Third Party Forks
------------------------

- aPerf
- Forge Perms
- Tick Profiler
- KCauldron
- ModControl
- HQM

Misc
----

- AutoClassLoader
- HQM Reset
- TileEntList

Other
=====

.. _ref-watchdog:

Watchdog
--------
Our live monitoring system. If a server is getting into trouble it barks. Build for the Amdins, but public to everyone. Each server sends a heartbeat every 20 seconds including live information about its condition.

* ``Heartbeat`` - Last server respond. 
* ``P30/120/300/600`` - Average server performance over the last 30/120/300/600 seconds in percentage. (100% = 20TPS, 50% = 10TPS..)
* ``GC30`` - The garbage dump from the server in the last 30 seconds.
* ``S6/12/24`` - Server sessions over the last 6/12/24 hours. High numbers signalize that the server crashed/froze/restarted a lot.
* ``Uptime`` - How long the server has been up.
* ``Players`` - Amount of players online.
* ``Staff`` - Amount of staff online, hover for details (red = staff with operator permissions). 
* ``StaffSeen`` - Time passed since a staff member has been seen on this server.
* ``Worlds`` - Amount of worlds present (does not mean loaded).
* ``Chunks`` - Amount of chunks loaded across all worlds. <n>/p chunks per player with a 256 total tolerance removed (the overworld spawn is usually loaded).
* ``Entities`` - Amount of entities (Animlas, Monster, Villager, Items on the ground..) loaded across all worlds. <n>/p entities per player with a 128 total tolerance removed (the overworld spawn is usually loaded).
* ``TileEntities`` - Amount of tile entities (Machines, Chests, Cables/Conduits..) loaded across all worlds. <n>/p tile entities per player with a 256 total tolerance removed (the overworld spawn is usually loaded).

Watchdog can be found `here <https://mineyourmind.net/server-status.html>`_

Mark2
-----

Website
-------
The website can be found `here <https://mineyourmind.net/>`_
