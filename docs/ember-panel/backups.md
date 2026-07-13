---
description: How to make a backup of your Minecraft server!
---

# Backups

### What Makes Us Different?

Ember Host uses custom software for our backups to give us advantages over the default backup system (that comes with Pterodactyl): de-duplicated and incremental backups. Unlike other hosts like Shockbyte or Apex, this means that each individual backup taken will only include changes since the last backup — hugely decreasing the amount of time backups take after the first one is created. In other words, our backups are faster and saves storage!

### Creating a Backup

Here's how to make a backup - start by heading over to the backups tab on our [panel](https://panel.ember.host), and click `Create Backup`.

<figure><img src="../.gitbook/assets/Backups.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Backup Options.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Selecting files to include here will override the existing `.pteroignore`
{% endhint %}

### Creating Scheduled Backups

Schduled backups are simple - you can use our inbuilt schedules feature in our panel, which allows for automated backup creation at whatever times you specify. When you reach the backup limited, the oldest non-locked backup will be deleted to make space for the new one the schedule creates. Curious on how to create a schedule? Check out our page on [schedules](schedules.md)!

### Choosing Which Files Are Included in a Scheduled Backup

Go into the files tab of the panel. Then, click 'New File' -> type up your ignore patterns -> save it as `.pteroignore`

```gitignore
backups/
bluemap/web/maps/**/tiles/**
dynmap/web/tiles/**
crash-reports/
logs/
```

The `.pteroignore` file uses the same pattern format as `.gitignore`. Each line is a pattern for files or directories to exclude from backups. Patterns are relative to the root of your server directory.

`backups/` ignores the entire backups directory and all its contents.

`bluemap/web/maps/**/tiles/**` ignores all tiles directories nested within the bluemap directory, including their contents.

`dynmap/web/tiles/**` ignores all content within the dynmap web tiles directory.

`crash-reports/` and `logs/` ignore those directories and their contents.

To negate (include) a previously excluded pattern, prefix it with `!`.

### Further Examples

To exclude a specific directory: `path/to/directory/`

To exclude all .log files: `*.log`

To exclude a file: `filename.txt`

To negate (include) a previously excluded pattern: `!important-file.txt`

To exclude everything except a specific directory:

```gitignore
*
!important-directory/
!important-directory/**
```

By `@andyishereboi`, `@goldenedit` and `@icewaffles`
