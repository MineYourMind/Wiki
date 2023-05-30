.. _ref-griefdefender:

++++++++++++++++++++++++++++++++++++++++++++++++++++
GriefDefender (protect your land) [Work in Progress]
++++++++++++++++++++++++++++++++++++++++++++++++++++

.. image:: https://i.imgur.com/9yf2Cf2.png
  :height: 120px
  :align:  right


Create a claim
==============
You have three options for creating a claim:

* Placing a chest will automatically create a basic claim around it.
* Right clicking the ground with a golden shovel will set the first corner of a claim. Click on the opposite corner of the desired area to set the second corner of the claim. Note: Minimum claim size is 10x10.
* Use the command ``/claimcreate [radius]`` to create a claim around where you are standing.

The glowstone and gold show you the corners which you can hide with a stick if you right click on the outside of your claim or you click on the inside to show them.

Toggle the Claim Tool
=====================

On some servers the claim tool may be toggled off by default to prevent interfering with certain mods that require use of a stick. Use the command ``/claimtool`` to toggle the golden shovel and claim inspection stick functions on and off.

Trust a player
==============

To grant someone the permissions to build in your claim you have to use the command ``/trust [Player]`` while you are in your claim. If you run the command in the outside then the player get trusted in all your claims.
It is also possible to revoke the permissions, for this you have to use ``/untrust [Player]``.

Deleting a claim
================

You can delete one claim or all claims. To delete a claim you have to stand in the claim and use the command ``/abandonclaim``, use it again to confirm it. If you want to delete all your claims you need to use the command ``/abandonallclaims`` and use the command again to confirm it.

Locate and Inspect claims
=========================

You can locate nearby claims by right clicking the ground with a stick. This will inform you of any nearby claims in the chat window. If you are standing inside a claim it will give you information about the current claim and its owner. 

Chat GUI and Toggling Claim Flags
=================================

All of GriefDefender's functions and commands can easily be found in it's chat GUI. This can be opened with the command ``/claiminfo``. Clicking through it's various tabs will give you access to commands, detailed claim info, claim flags, the trustlist, and other options.

.. image:: https://i.imgur.com/mRDaaAj.png
  :height: 120px
  :align:  right

Among it's many features, GriefDefender allows us to give players the ability to toggle certain claim flags themselves. This will allow you to decide whether players can enter claims, open chests, if monsters will spawn, water will flow, and nearly every other claim option. This is a very powerful feature and should give you near complate control over your claims. 


Commands
========

* ``/Trust [Player]`` - Gives the player permissions to build
* ``/TrustList`` - Lists all trusted players
* ``/UnTrust [Player]`` - Revokes any permissions of the player
* ``/claiminfo`` - Displays general info about the claim you are standing in. 1.10+ only
* ``/claimlist`` - Displays all claims you have access to. 1.10+ only
* ``/AbandonClaim`` - Deletes the claim you're standing in.
* ``/AbandonAllClaims`` - Deletes all of your claims.
* ``/AccessTrust [Player]`` - Gives a player permission to use your buttons, levers...
* ``/ContainerTrust [Player]`` - Gives a player permission to use and open everything.
* ``/PermissionTrust [Player]`` - Grants a player permission to share his permission level with others.
* ``/Untrust All`` - Removes all permissions for all players in your claim.
* ``/SubdivideClaims`` - Switches your shovel to subdivison mode, so you can subdivide your claims.
* ``/BasicClaims`` - Puts your shovel back in basic claim mode.
* ``/sellclaimblocks <amount>`` - Sells claimblocks for MyM's, 1:1 Ratio.
* ``/buyclaimblocks <amount>`` - Buys claimblocks for MyM's, 1:1 Ratio.

