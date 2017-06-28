Performance Guide
=================

Server Performance and Stability is the main goal of MineYourMind, the part we value the most and put most of our time in.
While we can take care of the outstanding things, the general usage depends on the setups from players and their understanding of modded minecraft performance. Therefore please take the time to read up on the following guides and do your duty on performance optimisation to keep the gaming experience as lag free as possible.

.. note::
   If you are enclined to have us take a look at your base or one you find suspicious, please let us know.


Applied Energistics
-------------------

As you can imagine, the performance impact of an Applied Energistics ME-System is mainly related to the size of the System. But there are parts with a bigger impact than others. There a lot of possible optimizations with less downsights - in some cases even quite some benefits - and easy implementation. This guide has been created to give an idea of how the system works and how to get the most out of it in terms of performance.

Basics
^^^^^^

Considering all parts of an ME-System it is clear that nearly every task is - be it crafting, export, import, machine control.. - is directly related to the inventory. This being pointed out, the biggest performance optimisation potential is within the size of the inventory. So what can be done, what are our recommendations?

.. note::
   When we speak about the **inventory** we are talking about the following parts: ME-Drive's, Storage Disk's and occupied slot's of those disk's. This means a system with only 10 items and 1000 ME-Drive's is not well performing (experience from Agrarian Skies, normal ME but 1000 Drives = 2/20 tps). So the goal is to keep all 3 of those parts as small as possible. E.g. 1 Drive and only fully occupied disks.


Split up
^^^^^^^^

The biggest performance saving potential lays within splitting things up. There is no need to have everything within one system. Of course, it is the most economical and comfortable way but in terms of performance it also is the worst. When I talk about splitting things up, this doesn't mean that everything should become over complicated. 

**The goal** to keep systems which are performing a lot of tasks as small as possible.

======================  ==========  =======  =============
#                       Automation  Storage  Autocrafting
======================  ==========  =======  =============
Storage size            Small       Big      Minimal
Machine automation      Yes         No       Only highly required (better fed by automation system)
Long time storage       No          Yes      No
Trash, overproduction   No          Yes      No
Tools, machines, drops  No          Yes      No
Mass autocrafting       No          Yes      Limited (for simple things, check out ender io autocrafting, or crafting table pipe automation -> even faster)
Onetime crafting        Yes         No       No (not enough resources)
Per resource limit      60k         None     60k (see the note below)
======================  ==========  =======  =============

.. note::
   The resource limit is related to the size of the storage disk. 60k in case of the biggest one. We only want to occupie one slot per resource type. A good way to still have access to everyting is to put the surplus into deep storage units. Once the ME-Systems storage drops below 20k it gets auto refilled from the deep storage unit...


**Automation** is our main system. It's job is the automation of the machinery. As it is performing hundreds of tasks per tick, its inventory size is as small as possible.

**Storage** is our long time storage vault. It is used for all the stuff not necessarily needed in the automation system. Here we will store things like, over production, tools, mob drops, enchantments, bees, non automation needed resources...

**Autocrafting** is our crafting setup for mass production. Its inventory is the as minimal as possible and only connected machines being related to autocrafting. Preffered would be to supply the system with the required ingredients. As mass production recipes are often quite simple a crafting table setup with pipe/conduit automation or a autocraft from for example ender io, can be faster, smaller and simpler.

.. warning::
   On **1.6.4** there is an issue with the autocrafting. If the required resources are not available the task is not being paused and will try over and over again. This is often extremly resource intense. Please be aware and keep an extra eye on it.


Specific
^^^^^^^^

Once you get to a big base automating multiple mods it often is not a lot to ask you to split it up even more. Have a single setup for bee automation, one for ore pre processing, one for energy production...


Ancient Warfare Automation Tree Farm
-------------------

There are only a few things to check to set up those farm correctly. If you don't follow these steps they can drain the performance of the whole server.
 - Make sure you have enough power so the Farm can cut down the trees as soon as they spawn. (use Flywheels to store the energy)
 - Never let the output inventory get filled up else the machine stops working and will still try to cut down trees
 - Please only use a size you can handle with your machine/energy


Active Tile Entities
--------------------

.. note::
   Tile entities are blocks being able to do a bit more than just being around (Chest, machine, lamp...). In this case we have to further split it up. There are active and passive tile entities. The active ones are ticking while the passive ones are not. So for example all those machines doing production are active and carpenters blocks inactive.

Mods are adding more and more tile entities, modpacks are getting bigger and bigger, with this the amount of active tile entities is rising to an amount of getting a bottleneck. While those tile ents might perform great on their own, they are causing limits within base mincraft code. E.g. there is a list storing all those active tile entities. This list gets updated on for example chunk load and unload either adding or removing entries. As the list grows with the age of the server, these tasks take longer and longer ending up causing constant lagg and major lag spikes (player login -> base load -> tile ents being added or teleport -> base unload -> tile ents being removed..)

**The goal** is to keep the amount of active tile entities as small as possible. 

**In Numbers** on a medium to big modpack we talk of about 30k active tile ents and 80k inactive with 10 players. At this rate the server impact is at about 30% while the tile ents on their own are only at about 2-5%.

This being quite a difficult topic, lets split it up:

Type of Tile Entities
^^^^^^^^^^^^^^^^

There are **Simple/Build/Environment blocks** like Sky Blocks, Canvas, Arcane Lamps, Ender IO Lamps.. Those are called tile entities. The first two mainly used as build blocks appear in values of hundreds and thousands in single bases. The lamps not being there so often spawn light tile ents around them. Those tile ents are not visible and only their only job is to give the light. One lamp is spawns around 30-80 tile ents.

**Conduits/Cable/pipe/tube** are necessary and have a lot of jobs. Nearly all of them are active tile ents. The only inactive one I know are IC2 cables and Applied Energistcs. As soon as possible it is recommended to switch to those. Next to this, keep things small and simple. Try to save as many conduits as possible. E.g. use high tier with high throughput, make use of enderchests and tesseracts for long distances, build your machines compact and switch to Applied Energistics as soon as possible.

**Multiblocks** while there are many nice multiblock structures, many of them are active. So consider for yourself if you can use a drum instead of a railcraft tank with 150 parts/tile ents for example.

**Machines/Flowers** in the end the amount of machines, including things like botania flowers, thaumcraft cystals... are so many needed, is it possible to upgrade them in speed, is there a faster one from another mod.. ?


Known performance eater
-----------------------

.. todo::
   Known performance eater


How to increase Client FPS
------

**Basic Minecraft**

To increase your FPS on many of our modpacks, firstly you will want to open your favourite modpack and go to options.
From there you will need to go to the options tab on the menu.
From there you will want to go to Video settings and do the following:

Set graphics to FAST.

Set View Bobbing to OFF.

Set Clouds to OFF.

Set Particles to MINIMAL.

Set Render Distance to 6 OR BELOW.

Set Smooth Lighting to OFF.

Set V-Sync to OFF.

Make sure you have no resource packs on.

Other ways to increase your FPS include downloading performance inhancers such as Fastcraft which is on most MYM modpacks or even optifine.

.. todo::
   What options to select in Optifine and Fastcraft to increase FPS

**Mod specific:**

**Agricraft**

Agricraft sprinklers and water channels can cause huge client/FPS lag. Their particles can be turned off in the mods config. Still, even without the water particles, these sprinklers can be the cause of huge FPS and even TPS lags. Try using as few of them as posible.

**Immersive Engineering**

Immersive Engineering Waterwheels and Windmills have moving parts which can cause client fps issues when looked at if there are too many of them within your field of view.

**Item Pipes**

 Item ducts that aren't opaque from Thermal Expansion and Buildcraft pipes can dramatically reduce your fps as they both show items moving through the pipes. These tile entities can drastically lower your fps, if you are using the clear item ducts from Thermal Expansion. If possible try to use the opaque ones as they are better for your fps and don't show the items moving through the pipes but work at the same transfer rate. 

As for Buildcraft, try using pipes from other mods which don't show the items. These days most mods work with just about any machine. If your setup requires BC pipes for whatever reason, try using as few of them as possible. You can also just use BC pipes as entry and exit point of your piping system and then switch to opaque Thermal Expansion ducts, as they will interconnect.

.. todo::
   Client performance guide. (get the most out of it)
