---
title: Access to scientific papers while not in university network
date: '2012-08-22'
description:
categories: network, unix, tricks
---

Publisher of scientific papers identify universities by their IP-Adresses, so you can access journals your university subscribed without providing any password. Thats a nice thing, but what when you are at home or travelling and you urgently _need_ that one paper?!

You can use a *tunnel*! The only requirement is a ssh-account on the server of your university.

<pre class="prettyprint">
ssh -D 8080 -f -C -q -N username@sshserverofyouruniversity.com

explanation:
-D 8080 : local dynamic application-level port forwarding, you can choose any non privileged port (above 1023)
-f : fork process in the background
-C : compression
-q : quiet mode
-N : no commands will be sent
</pre>

This tells your computer to relay all connections on local port 8080 to your university and back so the publisher only 'sees' the university and delivers your paper.

Now we only need to tell our browser to use that tunnel:
In Firefox this is  on the advanced tab - Network - Connection - Preferences
Then select manually and in SOCKS-Host: insert 127.0.0.1 and specify the port you selected earlier (i.e. 8080).

Now you can check http://www.whatsmyip.org/ and you should see the adress of your university server there.
Voilá - you now have access to all the websites your university has.
