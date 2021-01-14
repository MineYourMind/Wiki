Applied Energistics
+++++++++++++++++++

.. image:: https://i.imgur.com/twkm7S9.png

As you can imagine, the performance impact of an Applied Energistics ME-System is mainly related to the size of the System. But there are parts with a bigger impact than others. There a lot of possible optimizations with less downsights - in some cases even quite some benefits - and easy implementation. This guide has been created to give an idea of how the system works and how to get the most out of it in terms of performance.

We will do this by following some basic rules:

===============================
Proper AE2 System Design Rules:
===============================
* All items are stored in one (and only one) place.
* All devices on the network need to have one (and only one) possible route to the controller.
* All external storage devices need to be prioritized, dedicated and have overflow protection.

In addition to these rules, there are a few more things that can be done to better your performance;

* Special Designs: Sub-networks & P2P Tunnels
* Split Systems (Smaller systems dedicated to specific tasks)
* What not to store

Let's start with the 3 first ones;

====================
Stored in one place:
====================

Your job is to make sure the system never has to figure out where anything goes. Items you know you will get in the 10s of thousands should really have a dedicated storage device. You can use a pre-formatted cell in the ME Drive but it is usually better to just give it a dedicated DSU, Jabba Barrel or Storage Drawer. All three have the advantage of being able to either handle overflow (see below) or in the case of the DSU have such a high storage limit you can leave it alone for your entire career on the server.

In truth you don't need massive storage cells in your system at all. Even the largest bases can easily get by with 16k cells as long as you are handling the high volume items outside of the system. An easy way to tell is just to look at the storage cells every so often. If you are using all the slots but only using 50-70% of the space, then you still have room and the system can manage. But you should act whenever they start to get 100% full.

Any time a storage cell goes in the red (totally full) then you should automatically know you have a problem you need to fix. Time to upgrade to the next size storage cell - or take out the item that is sucking all that space and put it into external storage. You can always connect those external devices to the network via a Storage Bus and you can even make it efficient (see below). Just remember to flush those items out of the ME system as you are setting it up so nothing remains in a drive to confuse the network. This can be done by using the "ME IO Port".

============================
One Route to the controller:
============================

AE2 devices auto-connect. This is a great feature. But it also means that they connect even if you don't want them to and you can get cross connections. Sometimes these connections will still work and everything will look fine. But the system now has to figure something else out, and that takes computational time for the server.

Any time there are two routes to the same storage block, the network has to determine the best route it should use for that packet of items. Individually, that decision is made pretty quickly. But having to make that decision 50 times a second for hours on end because you are pumping tons of cobble and ore into your setup from 3 Ender Quarries will turn into a mountain of little decisions very quickly.

Because the different network components auto-connect this is really easy to get wrong. Most commonly this happens behind a large array of already connected Drive Bays where one cable will run across several of them in a row. It is also common to see this when the same cable runs in a small circle to connect 4-8 Devices that form a small wall. This causes the system to make minor routing calculations for everything that goes into them and if you are processing high volumes of items those minor calculations will add up. Carry a stack of cable anchors around with you and it you think there is a routing issue then just stick an anchor down to correct it. If it would work with an anchor between two cables then it should probably have an anchor there. And if it turns on without a cable physically connected to it then it usually doesn't need it.

=========================================================
Dedicated and prioritized external storage with overflow: 
=========================================================

Configuring your ME Storage Bus is easy. If you're using a dedicated storage block (like a DSU) then you just click the two wrenches on the Storage Bus' configuration UI.

The first wrench sets the item type so the network knows in advance that this item is stored in that device. This is important because if the network doesn't know up front then it has to figure it out while the item is in process.

The second wrench allows you to set the priority for that storage. The default of the system is 0 (zero). So anything over zero, even 1, is better. Not the system is always prioritizing storage even when is not changed. If you have 2 chests and one is closer then it will use the closest one. If the one further away is given a bit more priority then it uses the farther one. The distance is always part of the check routine though and it has an effect on the priority the controller assigns to the routing of the item.

For large systems that have long cable runs using 1 as a priority really isn't enough. My advice in game is always to think in the 100s when setting priority. All permanent, dedicated storage should just be given a moderately high priority level (like 100 or 200) to ensure that the cable runs and future sub-networks don't interfere with them.

Lets take a common example. You have 7 DSUs plugged into your network on storage buses to process most of the common quarry blocks away from the disk drives into a better storage mechanism. Those DSUs are on the other side of your base just to put them out of the way or to hide them. That chunk is a couple chunks away from the ME Controller that runs the system. If you use set the priority 100 for all the buses then you can be sure that it will always use those DSUs for storing those items as long as they are connected to the network.

The last topic for dedicated storage is "overflow protection". This basically means that your system will deal well when the dedicated storage device runs out of storage room. DSUs have such a high limit that most people would never exceed them so they are considered inherently overflow-proof for most players. For Jabba Barrels and Storage Drawers or similar mass storage blocks though you want to leave some upgrade space for a Void Upgrade.


==================
Inputs and Outputs
==================

Thought also needs to be put into how you are pumping items into or out of a system. A bad design sitting idle is usually not a problem. But a bad design that is pulling or pushing multiple stacks per second of blocks is going to cause havoc on a poorly designed AE2 network.

The typical setup for a quarry is to pump all the goods into an Ender Chest connected to one ME Input Bus and then let the system figure it out from there. And this works most of the time. But then you add a couple more quarries and an an 8 spawner mob grinder and 8 automated speed farms and now you have a lot of volume getting pumped into the system via that same chest and input bus. If your system doesn't follow the above rules then you will definitely have lag. But even if you follow the rules you may still find the volume is too great. So then what?

The answer depends on where is the volume coming from. If it's a quarry then you should filter out the cobble or stone before it gets to the input bus. If it is a massive tree farm the you want to filter out the logs. Just because you have this super flexible ME system doesn't mean you should use it for everything!

Another good way to avoid lag is to bypass the AE2 system entirely when importing items. A way you can do this is by sending all quarry items, via an Enderchest to one or more Storage Drawer setups, that are not connected to the AE2 network.

What i like to do, is make to send the items via Enderchest to two different storage drawer setups;

* The first setup will only contain ores that can be thrown directly into my ore processing, such as Iron, Copper, Lead etc. via another Enderchest. After being processed into ingots, these items can be imported directly into your AE2 system by inserting them into an ME Interface via an item transfer cable. What i like to do instead of that, is to use yet another Ender Chest to send my ingots to a Storage Drawer Setup with Compacting Drawers and a High Priority Storage Bus on the Controller, as this will let me directly access Nuggets, Ingots and Blocks of the materials stored in this setup.

* The second setup will contain all the ores that do not go into the normal ore processing, such as Diamonds, Emeralds, Coal and so on. This network you can either sort into multiple new Ender Chests with filters, that will then send them to the correct processing machines. An easier method, though slightly laggier, is to attach a high priority Storage Bus to the Drawer Controller so that these ores are available in your system. At the correct processing machines you can then place an ME Interface and slot the ore in the top 9 slots, as this will make the interface request that item to be sent there, which you can then extract with your transfer cable of choice into your machine setup.

===========================================
Special Designs: Sub-networks & P2P Tunnels 
===========================================

Subnets are a special class. The truth is subnets exist to improve performance and storage efficiency. The problem is if you set them up wrong then they can actually be horrible lag generators. So use them sparingly and work with someone who really knows how to set them up before you try and use them for mass production.

P2P Tunnels were also added to improve network design and configuration. The number of machines and devices you can fit onto a single network is actually mind boggling.


=============
Split Systems
=============

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
   
=====================
Other sources of Lag:
=====================
* One of the other things that can cause an AE2 system to lag, is to store Unstackable Items in it. It is highly recommended that you only store items that can stack, meaning do not use an AE2 system to store unsorted drops from your mobfarm, as these will give you loads of low durability, unstackable items. These items should be filtered beforehand, and either recycled or trashed.

.. image:: https://i.imgur.com/itwqtpZ.png
