---
description: How to install plugins to customize your server!
---

# Installing Plugins

### Introduction

> **Requirements**[**​**](https://docs.bloom.host/#requirements)
>
> In order to run plugins on your server, you have to be using a fork of Bukkit (e.g. Spigot, Paper, Pufferfish, Purpur, etc).  We recommend using [Paper](https://papermc.io). If you wish to use mods to customize your server instead, see our guide on [installing server mods](../mods/installing-mods.md)!

> **What are plugins?**[**​**](https://docs.bloom.host/#what-are-plugins)
>
> Plugins are essentially addons that make changes to your Minecraft server. These changes can be as minor as adding a simple command, or as major as adding an entire minigame to your server.

### Setup

{% hint style="danger" %}
**Warning!**&#x20;

Make sure you trust the source of your plugin! Malicious plugins can cause a considerable amount of damage to your server - so avoid downloading plugins from unknown/untrusworthy sources or 'leak' websites!
{% endhint %}

1. You'll first need to find the plugin you wish to install. Downloads for most plugins are found on [SpigotMC](https://www.spigotmc.org), [Bukkit](https://bukkit.org) or [Modrinth](https://modrinth.com/plugins).
2. Download the plugin to your local machine.
3. In your server's root directory, locate the `plugins` folder. Navigate into this folder, and upload your plugin's file there. Plugins can either be uploaded via our [web panel or through SFTP](../ember-panel/file-management.md).&#x20;
4. Restart your server (never do `/reload`!), and your plugin should be successfully installed!

Once the server is online, type `plugins` in your console or `/plugins` in-game. If you're able to see the plugin that you just installed show up in green, then you're good to go!

### [​](https://docs.bloom.host/#what-to-do-if-a-plugin-doesnt-load)Troubleshooting <a href="#what-to-do-if-a-plugin-doesnt-load" id="what-to-do-if-a-plugin-doesnt-load"></a>

If your plugin doesn't install properly, see if the following steps solve your issue.

1. **Check the plugins folder**: Confirm that your plugin has been uploaded to the `plugins` folder, and not accidentally uploaded elsewhere.
2. **Check your startup logs**: While your server starts up, see if there's any errors or warnings about your plugin in console. These often tell you why your plugin did not start up properly.&#x20;
3. **Check the plugin's version**: Make sure your plugin version matches your Minecraft server version! If your plugin is incompatible with your server version, it won't function properly. You can check what versions your plugin support from the website you downloaded it from, or you can ask the plugin's author.

By `@icewaffles`
