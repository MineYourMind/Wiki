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

Backup
------

ChunkManager
------------

Claim/Island Deleter
--------------------

Redis Chat
----------

Stats
-----

Announcer
---------

Vote
----

Random Teleport
---------------

Ranks
-----

ForumFeed
---------

MultiBlockLimit
---------------

Forum/Ticket InterOp
--------------------

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

World Downloader
----------------

EntityControl
-------------

Chunk Deleter
-------------

MyM-Tweaks
----------

MyMKit
------

ModPatches
----------

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
Our live monitoring system. If a server is getting into trouble it barks. Build for the Amdins, but public to everyone. Each server sents a heartbeat every 20 seconds including live information about its condition.

* ``Heartbeat`` - Last server respond. 
* ``P30/120/300/600`` - Average server performance over the last 30/120/300/600 seconds in percentage. (100% = 20TPS, 50% = 10TPS..)
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
