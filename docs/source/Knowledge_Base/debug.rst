+++++++++++++++
Debugging Tools
+++++++++++++++


Performance & Threads
=====================

**Getting Started**

1. Make sure you have JDK (Java Development Kit) installed - JRE (Java Runtime Environment) is not enough to run VisualVM. You can download the latest version of JDK `here <http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>`_
2. Download `VisualVM <http://visualvm.java.net/download.html>`_
3. Extract the downloaded archive and start VisualVM (\visualvm_138\bin\visualvm.exe)
4. When Minecraft is running, `on the left side under "Local" <https://i.imgur.com/j7h971G.png>`_ you should see either ``net.minecraft.client.main.Main`` or ``net.minecraft.launchwrapper.Launch`` - double click it

**Performance**

To profile your client performance, do the following:

1. Select the ``Sampler`` tab and click on the ``CPU`` button
2. Let it run for ~5 minutes, then click ``Stop``
3. Click on ``Snapshot`` to open the profile data
4. Click on the first button (``Export to...``) and save the file
5. Zip the exported file and send it to us.

**Threads**

To find out what Minecraft is doing at the moment, do the following:

1. Select the ``Threads`` tab and click on the ``Thread Dump`` button
2. Copy everything by pressing ``Ctrl + A`` & ``Ctrl + C``
3. Paste it on `Pastebin <http://pastebin.com>`_
4. Click on the ``Create New Paste`` button and copy the web link
5. Send the link to us

Connection
==========
1. Download `WinMTR <http://downloads.sourceforge.net/project/winmtr/WinMTR-v092.zip>`_
2. Type the server address into the ``Host`` box and click ``Start``
3. Click ``Stop`` after 5 minutes
4. Paste it on `Pastebin <http://pastebin.com>`_
5. Click on the ``Create New Paste`` button and copy the web link
6. Send the link to us
