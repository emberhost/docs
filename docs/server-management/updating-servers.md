---
description: How to change the version of your server!
---

# Updating Servers

## How to Update Your Server Version

The process for updating the Minecraft version of your server is actually incredibly easy. The following guide contains instructions corresponding to different server platforms.

### On PaperMC

1. Go to Paper's [website](https://papermc.io).
2. Download the latest build (of the version you want).
3. Rename the file to `server.jar` or whatever you specified your server JAR file name to be in the startup tab of our panel.
4. Replace the current `server.jar` in your server files with the new one you just downloaded.
5. Restart/start your server.

### On FabricMC

1. Go to FabricMC's [server launcher download website](https://fabricmc.net/use/server/). 
2. Select the Minecraft version and Fabric loader version that you wish to update to, and download it.
3. Rename the downloaded file to `server.jar` or whatever you specified your server JAR file name to be in the startup of our panel. Alternatively, you can leave the file's name as it is and change the server JAR file name in the startup tab of the panel to be that of the downloaded file.
4. Replace the current `server.jar` (or whatever your server launcher file currently is) with the new server JAR you have just downloaded.
5. Restart/start your server.


Any new chunks generated should now contain new world generation if applicable, and you're now running the newer Minecrat version you want.

## How To Downgrade Your Server Version

This process is technically not possible, and updated worlds cannot be downgraded. The only 'real' way to downgrade is to restore from a backup. However, if you don't need to keep your world files and don't have a backup, follow these steps.&#x20;

1. Stop your server.
2. Change your server JAR file to the version you want.
3. Delete the folders `world`, `world_nether` and `world_the_end.`
4. Restart/start your server.

By `@icewaffles`
