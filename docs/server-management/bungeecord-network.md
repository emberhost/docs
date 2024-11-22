---
description: How to link servers together with BungeeCord!
---

# BungeeCord Network

### **Why Would I Need This?**

When setting up a Minecraft server, you may want to have multiple accessible worlds. This can be accomplished by having each word/gamemode on a separate server, which is then all connected by a **proxy**. The proxy is what will be your players actually connect to - however, it does not actually run a 'real' server software on it. Interested? Read on...

{% hint style="warning" %}
**Waterfall** is now officially no longer maintained or supported by the PaperMC team. You should use [Velocity](velocity-network.md) instead. You can read their announcement [here](https://forums.papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/).
{% endhint %}

### **Download & Configuration**

Firstly, it's important to note we actually recommend using [Waterfall](https://papermc.io/downloads#Waterfall). Why? It's an actively maintained fork of BungeeCord by the PaperMC team which brings about both increased performance and numerous bug fixes! After you download the JAR file, upload it to your server and hit the restart button.

After the configuration files have been generated, open the `config.yml` and define the name, IP address, and port for each server you'd like to be a part of your network. Remember to set the 'main' port that you want users to connect with to be opened for the **proxy** server. You will also need to set the `ip_forward` configuration option to true in this file. For more information, read the [Waterfall configuration docs](https://paper.readthedocs.io/en/latest/waterfall/configuration.html).

Only some minor configuration needs to be done to your backend servers - the ones which BungeeCord/Waterfall actually sends your players to! Start by setting `online-mode` to `false` in each of your **backend** servers. You can find this setting in the `server.properties` file. Then, edit your `spigot.yml` files in said servers and change the option named `bungeecord` to `true`. Upon saving these edits, restart your backend servers to implement the changes.

### **Security**

There exists a BungeeCord (and thus Waterfall) UUID spoof exploit which allows users to join any of your backend servers without authenticating through the BungeeCord proxy - meaning they can join your server as any user. Thus, we recommend for you to download [BungeeGuard](https://www.spigotmc.org/resources/bungeeguard.79601/). Start by uploading the JAR into file to **both** your proxy and backend servers before restarting them. After you have restarted the servers you installed BungeeGuard on, locate your **proxy** server's BungeeGuard `config.yml` and copy the authentication token. Paste this authentication token into your **backend** server's BungeeGuard `config.yml` file.

Restart all your servers one last time and see if everything is working properly!

By `@icewaffles`
