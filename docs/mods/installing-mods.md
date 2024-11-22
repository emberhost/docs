---
description: How to install mods to customise your server!
---

# Installing Mods

### Introduction

> **Requirements**[**​**](https://docs.bloom.host/#requirements)
>
> In order to run mods on your server, you have to be using either [Forge](https://files.minecraftforge.net/net/minecraftforge/forge/) or [Fabric](https://fabricmc.net/use/server/). If you wish to use plugins to customise your server instead, see our guide on [installing server plugins](../plugins/installing-plugins.md)!

> **What are mods?**[**​**](https://docs.bloom.host/#what-are-plugins)
>
> Mods are like plugins: they're essentially addons that make changes to your Minecraft server. However, note that modded servers will generally be much slower than servers running Paper and its forks, due to Fabric and Forge not being designed with performance in mind.

### Setup

{% hint style="warning" %}
**Mod Compatibility**\
Ensure you're downloading the correct version of your mods! Forge and Fabric mods are usually not cross-compatible with each other (unless stated otherwise), and also often don't work across Minecraft versions.
{% endhint %}

1. You'll first need to find the mod you wish to install. Most mods can be found on either [Modrinth](https://modrinth.com/mods) or [CurseForge](https://www.curseforge.com/minecraft/mc-mods). It is not recommended to download any files from sites other than these!
2. Download the mod to your local machine. Mods can either be uploaded via our web panel or through SFTP.&#x20;
3. In your server's root directory, locate the `mods` folder. Navigate into this folder, and upload your mod's file there. Additionally, many **Fabric** mods require the [Fabric API](https://modrinth.com/mod/fabric-api). Download the relevant Fabric API for you server version, and upload this file into the same directory.&#x20;
4. Restart your server, and your mod(s) should be successfully installed!

Certain mods require players to install them on their client as well. Check the documentation of your mod to see if this is required; mods may provide a separate file for clients and servers.

By `@icewaffles`
