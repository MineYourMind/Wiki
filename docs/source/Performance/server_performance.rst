++++++++++++++++++++++++++++
Improving Server Performance
++++++++++++++++++++++++++++

Server Performance and Stability is the main goal of MineYourMind, the part we value the most and put most of our time in.
While we can take care of the outstanding things, the general usage depends on the setups from players and their understanding of modded minecraft performance. Therefore please take the time to read up on the following guides and do your duty on performance optimisation to keep the gaming experience as lag free as possible.

.. note::
   If you are enclined to have us take a look at your base or one you find suspicious, please let us know.

Reducing tile entities
======================

Once you get to a big base automating multiple mods it often is not a lot to ask you to split it up even more. Have a single setup for bee automation, one for ore pre processing, one for energy production...


Ancient Warfare Automation Tree Farm
------------------------------------

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
^^^^^^^^^^^^^^^^^^^^^

There are **Simple/Build/Environment blocks** like Sky Blocks, Canvas, Arcane Lamps, Ender IO Lamps.. Those are called tile entities. The first two mainly used as build blocks appear in values of hundreds and thousands in single bases. The lamps not being there so often spawn light tile ents around them. Those tile ents are not visible and only their only job is to give the light. One lamp is spawns around 30-80 tile ents.

**Conduits/Cable/pipe/tube** are necessary and have a lot of jobs. Nearly all of them are active tile ents. The only inactive one I know are IC2 cables and Applied Energistcs. As soon as possible it is recommended to switch to those. Next to this, keep things small and simple. Try to save as many conduits as possible. E.g. use high tier with high throughput, make use of enderchests and tesseracts for long distances, build your machines compact and switch to Applied Energistics as soon as possible.

**Multiblocks** while there are many nice multiblock structures, many of them are active. So consider for yourself if you can use a drum instead of a railcraft tank with 150 parts/tile ents for example.

**Machines/Flowers** in the end the amount of machines, including things like botania flowers, thaumcraft cystals... are so many needed, is it possible to upgrade them in speed, is there a faster one from another mod.. ?


Known performance eaters
------------------------

.. todo::
   Known performance eater