Applied Energistics
+++++++++++++++++++

.. image:: https://i.imgur.com/uDrRAvV.jpg

As you can imagine, the performance impact of an Applied Energistics ME-System is mainly related to the size of the System. But there are parts with a bigger impact than others. There a lot of possible optimizations with less downsights - in some cases even quite some benefits - and easy implementation. This guide has been created to give an idea of how the system works and how to get the most out of it in terms of performance.

Basics
======

Considering all parts of an ME-System it is clear that nearly every task is - be it crafting, export, import, machine control.. - is directly related to the inventory. This being pointed out, the biggest performance optimisation potential is within the size of the inventory. So what can be done, what are our recommendations?

.. note::
   When we speak about the **inventory** we are talking about the following parts: ME-Drive's, Storage Disk's and occupied slot's of those disk's. This means a system with only 10 items and 1000 ME-Drive's is not well performing (experience from Agrarian Skies, normal ME but 1000 Drives = 2/20 tps). So the goal is to keep all 3 of those parts as small as possible. E.g. 1 Drive and only fully occupied disks.


Split up
========

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