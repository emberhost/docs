---
description: How to link servers together with Velocity! Like BungeeCord, but better.
---

# Velocity Network

### **Why Would I Need This?**

Velocity exists because [BungeeCord](bungeecord-network.md) contains several flaws. Velocity is the fast and modern implementation of a proxy. It is complete recode — it is **not** a fork of BungeeCord (like Waterfall is).

{% hint style="success" %}
**Velocity** is our recommended proxy software. Not only is it faster and safer, Waterfall, our old recommended fork of BungeeCord by the PaperMC team, is [no longer maintained](https://forums.papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/).
{% endhint %}

### **Download & Configuration**

Start by downloading [Velocity](https://papermc.io/downloads#Velocity). After you download the JAR, upload it to your file directory and start your server. Make sure to delete any existing plugins from elsewhere, including BungeeCord!

After the configuration files have been generated, open the `velocity.toml` and define the name, IP address, and port for each server you'd like to be a part of your network. Remember to set the 'main' port that you want users to connect with to be opened for the **proxy** server. You should also use the `modern forwarding` configuration option in this file. For more information, read the [Velocity configuration docs](https://velocitypowered.com/wiki).

Only some minor configuration needs to be done to your backend servers - the ones which Velocity actually sends your players to! Start by setting `online-mode` to `false` in each of your **backend** servers. You can find this setting in the `server.properties` file. Then, go back to the proxy server and copy the secret key from `velocity.toml` before pasting it into your `paper-global.yml`'s Velocity section! Make sure to set `velocity-support` here in to true as well.

### **Security**

Unlike on BungeeCord, the security issue that the BungeeGuard plugin patches does not exist when using a Velocity server. Velocity's modern forwarding means you are safe from the UUID spoof exploit on all modern Minecraft versions!

If you have any more questions, you can receive support from either our knowledgable community or dedicated staff at any time of day in our [Discord](https://discord.com/invite/68s9zKtSFb). Good luck with your server!

{% embed url="https://ember.host" %}
