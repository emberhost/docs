---
description: How to link servers together with Velocity! Like BungeeCord, but better.
---

# Velocity Network

### **Why Would I Need This?**

BungeeCord is outdated and contains several flaws. Thus, Velocity is a complete recode and **not** a fork of Bungee (like Waterfall is) and a modern implementation of a proxy. However, please note that Velocity may have less supported plugins and is not as 'customisable' as BungeeCord and its forks. You can find out more about BungeeCord and networks [here](bungeecord-network.md).

{% hint style="success" %}
**Velocity** is our recommended proxy software. Not only is it faster and safer, Waterfall, our old recommended fork of BungeeCord by the PaperMC team, is [no longer maintained](https://forums.papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/).
{% endhint %}

### **Download & Configuration**

Start by downloading [Velocity](https://papermc.io/downloads#Velocity). After you download the JAR, upload it to your file directory and start your server. Make sure to delete any existing plugins from elsewhere, including BungeeCord!

After the configuration files have been generated, open the `velocity.toml` and define the name, IP address, and port for each server you'd like to be a part of your network. Remember to set the 'main' port that you want users to connect with to be opened for the **proxy** server. You should also use the `modern forwarding` configuration option in this file. For more information, read the [Velocity configuration docs](https://velocitypowered.com/wiki).

Only some minor configuration needs to be done to your backend servers - the ones which Velocity actually sends your players to! Start by setting `online-mode` to `false` in each of your **backend** servers. You can find this setting in the `server.properties` file. Then, go back to the proxy server and copy the secret key from `velocity.toml` before pasting it into your `paper-global.yml`'s Velocity section! Make sure to set `velocity-support` here in to true as well.

### **Security**

There is no longer a security issue as with BungeeCord when on a Velocity server. Velocity's modern forwarding means you are safe from the UUID spoof exploit on all modern Minecraft versions!

By `@icewaffles`
