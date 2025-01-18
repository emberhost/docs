---
description: >-
  Experiencing lag? Try adjusting some settings to improve performance without
  compromising on gameplay!
---

# Server Optimization

### **Ember Host Optimization Guide**

The first thing to keep in mind is that there is no "best" configuration. These values will only improve performance to a certain degree - you should increase or decrease them to adjust to your server’s needs. However, it should be noted that the values provided below aim to be close to vanilla as possible, unlike certain more aggressive guides.

### **Server Software**

{% hint style="info" %}
**Note:** \
Before you check out our recommended server softwares, please note the given playercounts do **not** apply to everyone! They're just a generic estimate: how many players your specific server can handle will differ.
{% endhint %}

<10 players - [Vanilla](https://www.minecraft.net/en-us/download/server/) | Standard Minecraft software distributed by Mojang.

15-50 players - [Paper](https://papermc.io/) (recommended) | Actively provides dupe and bug fixes over vanilla Minecraft. It contains many optimization patches and is designed with performance in mind.

50+ players - [Pufferfish](https://ci.pufferfish.host) | Contains optimizations Paper considers too 'extreme' to add. Not recommended for use unless you have a very large server and require the extra performance.

50+ players - [Purpur](https://purpurmc.org/) | Purpur is based off Pufferfish, meaning it contains all of its extra optimizations. Only use Purpur if you need its configuration options! Not recommended if you generally want a 'vanilla' MC experience.

### **Chunk Settings**

`server.properties - view-distance: 7` The view distance option is the most impactful option on server performance. This option controls how many chunks the server will load around players and how far they will be able to see. For servers with under 10 players, setting this value to 10 or higher can be acceptable. This option should never be reduced below 3.

`server.properties - simulation-distance: 5` Simulation distance controls how many chunks around the player will tick. If you don't want to lower the view distance any further but would like to avoid chunk lag, decreasing this option can help. You should never have this option set higher than the view distance.

`paper-world-defaults.yml - prevent-moving-into-unloaded-chunks: true` This option will prevent players from entering chunks that are unloaded by forcing them back. If players were allowed to move into said chunks, it would cause a load on the main thread and create a lag spike. Pre-generating chunks is recommended! Try a plugin like [Chunky](https://www.spigotmc.org/resources/chunky.81534/).

### **Entities**

`bukkit.yml - spawn-limits` This option controls the amount of mobs per-player the server will spawn. Adjust this value as needed! If you need more animals, increase animals. If you need more zombies, increase monsters. This section is also the best and simplest one for limiting entity lag.

`monsters: 30` `animals: 7` `water-ambient: 7` `water-animals: 3` `water-underground-creature: 3` `axolotls: 3` `ambient: 1`

`spigot.yml - mob-spawn-range: 4` This option controls the maximum distance from a player that mobs will spawn, in chunks. This should always be lower/equal to your simulation distance.

`spigot.yml - nerf-spawner-mobs: true` This will result in mobs losing their AI if they spawned from a mob spawner. Consider leaving this option to false to preserve a more ‘vanilla’ experience for players, as this option is obviously very noticeable.

`paper-world-defaults.yml - per-player-mob-spawns: true` This option has little impact on performance. However, if enabled, it ensures the server distributes mobs evenly to each player. This means a single mob farm won’t be able to fill the server’s mob cap!

`paper-world-defaults.yml - max-entity-collisions: 2` This option will reduce the amount of work the server does to compute collisions between entities. However, this will screw with the entity cramming gamerule – set this value equal or greater than your gamerule’s value if that’s important for you!

`paper-world-defaults.yml - update-pathfinding-on-block-update: false` This reduces the amount of pathfinding mobs do, as they do not recompute pathfinding upon a block update. Do note that mobs will appear to be slightly laggier if this is enabled.

`paper-world-defaults.yml - fix-climbing-bypassing-cramming-rule: true` This fixes a vanilla bug where the entity cramming gamerule doesn’t affect mobs on vines/ladders. It does break vanilla behaviour, so this option is very much up to you.

`paper-world-defaults.yml - mob-spawner-tick-rate: 2` This option controls the frequency at which spawners will attempt to spawn mobs. A value of 2 is practically impossible to notice as a player. If your world has many spawners, you may want to consider increasing this number to 4, but you should avoid going higher because it can reduce spawn rates.

`paper-world-defaults.yml - armor-stands-do-collision-entity-lookups: false` This value simply prevents armour stands from participating in collisions. It is mostly used to prevent lag machines.

`paper-world-defaults.yml - disable-chest-cat-detection: true` When opened, chests scan if there’s a cat sitting on top of it. Do you really need this behaviour?

`pufferfish.yml - dab.activation-dist-mod: 8` This value controls how quickly the effects of DAB\* wear off with distance. This value should generally not be set below 6. If you have a smaller server, consider disabling DAB altogether to preserve vanilla behaviour.

> \*DAB stands for the Dynamic Activation of Brain. When entities are near to the player, they will tick like normal, but the farther away entities get, their AI will be ticked less and less frequently. These values can affect players’ mob farms, so consider increasing the activation-dist-mod parameter or disabling the feature altogether.

### **Other**

`paper-world-defaults.yml - nether-ceiling-void-damage-height: 127` There are two reasons for this. Firstly, if players are allowed onto the nether roof, they can roam freely and generate loads of chunks - causing lag. Secondly, the number of entities spawning on the roof will also be somewhat significant. Together, these reasons form a compelling argument to leave the nether roof disabled – however, it’s up to you to decide whether your server needs it – as it could be considered a ‘vanilla’ feature.

`paper-world-defaults.yml - optimize-explosions: true` When set to true, this option will perform explosions much faster! It is almost indistinguishable from vanilla – there is almost no reason to keep this value set to false.

`paper-world-defaults.yml – anti-xray.enabled: true` Paper’s anti-xray feature is one of the best around, and is our recommended go-to. It should be noted that engine 3 is recommended: it has a solid balance of being effective whilst minimising network issues for players with a weaker internet connection.

`paper-world-defaults.yml - enable-treasure-maps: false` Treasure maps are poorly implemented by Mojang and will cause a lag spike when generated. This is because it can sometimes hang the server if the ‘treasure' is in an ungenerated chunk. However, this is safe to enable if your entire map is pregenerated.

`paper-world-defaults.yml - redstone: ALTERNATE_CURRENT / EIGENCRAFT` When enabled, this option replaces the vanilla redstone algorithm with a far faster algorithm. Either algorithm is incredibly similar to vanilla and should have no noticeable differences in the majority of scenarios.

`paper-world-defaults.yml - grass-spread-tick-rate: 4` This option controls how quickly grass/mycelium spreads. This causes grass to spread more slowly, but will result in improved performance on servers where many chunks are loaded and grass is thus constantly spreading.

### **Tips**

• Timings is a simple way to see exactly what is lagging your server! As it's (v2) built into Paper, you just need to execute the `/timings paste` command and click the link you're provided with. If you're unsure how to read timings, check out this [video tutorial by Aikar](https://www.youtube.com/watch?v=T4J0A9l7bfQ). Note that timings may be removed from Paper, and we suggest for you to use Spark (see below!) instead.

• [Spark](https://github.com/lucko/spark) is a plugin that digs a bit deeper than timings and tells you exactly what's lagging your server through profiling your server's CPU and memory usage. You can read how to use it on its [wiki](https://spark.lucko.me/docs/).

• Avoid dodgy forks! Those downstream of Paper/Pufferfish/Purpur have been known to be shockingly unstable while providing a minor performance impact at best.

By `@icewaffles`
