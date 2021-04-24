+++++++++++++++++++++++
Superb Minecraft Habits
+++++++++++++++++++++++

A guide to optimize both client- and server-side performance.

TPS - Server Side
-----------------

In a multiplayer environment, it is important to keep individual loading times as low as possible. This means that setups must be optimized to minimize lag and maximize TPS (ticks per second).

TPS is optimally 20, meaning that a single server “tick” is 0.05 seconds. However, this is not always the case. Often, TPS will dip below 20, slowing everything down. As a player, you can check with ``/tps``, but do not spam it.

**TPS Ratings**
^^^^^^^^^^^^^^^

- ``20.0`` - Perfect
- ``19.95-19.99`` - Excellent - unnoticeable lag.
- ``18.5-19.94`` - Fair - Minor block and item delay.
- ``16.0-18.4`` - Average - This is expected with many players on a large modded server.
- ``<16.0`` - Bad - Report low TPS to #support in discord. Mentioning the playerlist and timestamp when the lag begins helps.

Ping and FPS - Client Side
--------------------------

Ping is the length of time data takes to travel between the client and the server. Distance and quality of connection will influence latency. MineYourMind servers are located in Germany. Check your ping with /ping.

**Ping Ratings**
^^^^^^^^^^^^^^^^

- ``1-90`` - Optimal
- ``91-179`` - Good
- ``180-299`` - Poor - Delay interacting with blocks/players/entities.
- ``300-499`` - Bad - Nearly unplayable.
- ``500+`` - Connection Issue - check internet quality, background tasks, or restart your device.

Do not confuse TPS with FPS! FPS (frames per second) is completely client side decided by the computer’s ability to render the minecraft world. However, extremely low FPS may be caused by the same issue that is hindering the TPS.

Resources
---------
There are documents you can follow to minimize your impact on the server.

 - `Performance Guide <https://docs.mym.li/en/latest/Performance/index.html>`_

 - `Best Applied Energistics Setup <https://mineyourmind.net/forum/threads/best-applied-energistics-setup.10888/>`_

 - `Tips on how to Increase your FPS <https://mineyourmind.net/forum/threads/tips-on-how-to-increase-your-fps.3929/>`_


If you are unsure if a setup is impacting the server in a negative way, don't hesitate to ask for help.

**Miscellaneous Tips**
 - Keep multiblocks away from each other and chunk boundaries
 - Do not put AE2 drives into portable storage 
 - Avoid nested AE2 systems (subnets with storage bus/interface)
 - Keep an empty biometric card with all permissions in your ME security terminal
 - Minimize use of agricraft and openblocks sprinklers
 - Eliminate cable/pipe loops
 - Do not have cable/pipes crossing chunk boundaries if not chunk loaded
 - Keep an eye on mob farms in case of item leaks
 - Do not put an entire base in one chunk - spread it out!
