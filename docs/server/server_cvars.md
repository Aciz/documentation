# List of ETJump server cvars
Below is a list of all ETJump related cvars (console variables) for server configuration.

---

## g_adminChat
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_adminChat             | 0 or 1        | 1

Toggles adminchat functionality on the server.

```{seealso}
[Admin chat](admin_system.md/#admin-chat)
```

---

## g_adminLog
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_adminLog              | filename      | adminsystem.log

Currently does nothing.

```{todo}
Make this log admin commands.
```

---

## g_allowSpeclock
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_allowSpeclock         | 0 or 1        | 1

Toggles whether players are allowed to use [`speclock`](../client/client_commands.md/#speclock-specunlock).

---

## g_autoRtv
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_autoRtv               | 0 - 1440      | 0

Sets the interval for calling automatic Rock The Vote, in minutes.

---

## g_banner1-5
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_banner1               | any text      | ETJump
g_banner2               | any text      | A Wolfenstein: Enemy Territory Trickjump Modification
g_banner3               | any text      | www.etjump.com
g_banner4               | any text      | Developed by Zero, Feengur and Setup
g_banner5               | any text      | Thanks for choosing ETJump!

Sets text for banners displayed on the server.

---

## g_bannerLocation
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_bannerLocation        | 0 - 3         | 1

Sets the location where banners are printed.

* **0** for center print, 
* **1** for top print, 
* **2** for chat print, 
* **3** for left print.

---

## g_bannerTime
Name                    | Values               | Default
:-----------------------|:---------------------|:------------
g_bannerTime            | any positive integer | 60000

How often in milliseconds to print banners.

---

## g_banners
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_banners               | 0 or 1        | 1

Toggles the banner system.

---

## g_blockCheatCvars
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_blockCheatCvars       | bitflag       | 0

Blocks usage of certain cvars that can be used to cheat. If the rules are violated, the player is moved to spectators.

* **1** forces `cl_yawspeed 0` & `cl_freelook 1`
* **2** forces `com_maxfps 25-125` when using `pmove_fixed 0`

---

## g_blockedMaps
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_blockedMaps           | map names     | 

A list of maps that cannot be voted for. Names are separated by space.

```{note}
Does not perform validation for mapnames.
```

---

## g_chatOptions
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_chatOptions           | 0 or 1        | 1

Allow players to highlight other players in chat using `@name@`.

---

## g_chatReplayMaxMessageAge
Name                      | Values               | Default
:-------------------------|:---------------------|:------------
g_chatReplayMaxMessageAge | any positive ingeter | 0

Maximum age for a chat replay message to be considered valid. If the message is older than the time specified here, it will not be included in the chat replay. Value **0** means messages never expire, and are always sent regardless of how old they are.

---

## g_customMapVotesFile
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_customMapVotesFile    | filename      | customvotes.json

Filename for the custom map votes file.

---

## g_dailyLogs
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_dailyLogs             | 0 or 1        | 1

Whether to log everything in a single file or change the file daily.

---

## g_debugTrackers
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_debugTrackers         | 0 or 1        | 0

Toggles tracker debugging. When enabled, all tracker changes are printed to players. Additionally, players gain access to [`tracker_print`](../client/client_commands.md/#tracker_print) and [`tracker_set`](../client/client_commands.md/#tracker_set) commands.

```{note}
Timerun records are not saved when tracker debugging is enabled.
```

---

## g_disableVoteAfterMapChange
Name                        | Values               | Default
:---------------------------|:---------------------|:------------
g_disableVoteAfterMapChange | any positive integer | 30000

How long players must wait to vote again in milliseconds after map changes.

---

## g_enableVote
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_enableVote            | 0 or 1        | 1

Toggles voting.

---

## g_floodlimit
Name                    | Values               | Default
:-----------------------|:---------------------|:------------
g_floodlimit            | any positive integer | 5

How many times can player send a message fast before flood protection kicks in.

---

## g_floodprotection
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_floodprotection       | 0 or 1        | 1

Toggles flood protection.

---

## g_floodwait
Name                    | Values               | Default
:-----------------------|:---------------------|:------------
g_floodwait             | any positive integer | 768

Time in milliseconds to allow player to send messages again.

---

## g_ghostPlayers
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_ghostPlayers          | 0 or 1        | 1

Toggles whether players can go through each other.

---

## g_goto
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_goto                  | 0 or 1        | 1

Toggles [`goto`](../client/client_commands.md/#goto).

---

## g_levelConfig
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_levelConfig           | filename      | levels.cfg

File to store admin system levels in.

---

## g_mapDatabase
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_mapDatabase           | filename      | maps.dat

File where information about maps is stored (eg. playtime).

---

## g_mapScriptDir
Name                    | Values         | Default
:-----------------------|:---------------|:------------
g_mapScriptDir          | directory name | mapscripts

Directory to load custom map scripts from.

---

## g_maxConnsPerIP
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_maxConnsPerIP         | any integer   | 2

How many clients can connect from a single IP address.

```{note}
[ETe](https://github.com/etfdevs/ETe) and [ET: Legacy](https://www.etlegacy.com/) also limit this with on the server side with `sv_maxclientsPerIP` and `sv_ipMaxClients`, respectively.
```

---

## g_motdFile
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_motdFile              | filename      | motd.json

File that sets the message of the day.

---

## g_moverScale
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_moverScale            | 0.1 - 5.0     | 1.0

Scales movement speed of entities following spline paths (typically vehicles) by the given value.

```{seealso}
[`!moverscale`](./admin_system.md#moverscale)
```

---

## g_mute
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_mute                  | bitflag       | 0

Sets restrictions to apply to muted players. 

* **0** default behaviour, cannot send chat messages
* **1** cannot send private messages
* **2** cannot call votes

---

## g_nameChangeInterval
Name                    | Values               | Default
:-----------------------|:---------------------|:------------
g_nameChangeInterval    | any positive integer | 60

How often in seconds is the name change limit reset.

---

## g_nameChangeLimit
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_nameChangeLimit       | any integer   | 5

How many times a player can change their name before getting kicked for spam.

---

## g_noclip
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_noclip                | 0 or 1        | 0

Toggles whether players have access to `noclip` command.

```{seealso}
[`!noclip`](admin_system.md/#noclip)
```

---

## g_nofatigue
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_nofatigue             | 0 or 1        | 1

Toggles whether players can have access to permanent adrenaline with the [`etj_nofatigue`](../client/etjump_cvars.md/#etj_nofatigue) cvar.

---

## g_oss
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_oss                   | bitflag       | 399

Indicates operating systems and architectures supported by the mod. Used by the ET: Legacy server browser to filter out incompatible servers for clients architecture.

* **0** vanilla/unknown/ET: Legacy auto setup
* **1** Windows x86
* **2** Linux x86
* **4** Linux x86_64
* **8** macOS x86_64
* **16** Android aarch64
* **32** Raspberry Pi arm
* **64** Raspberry Pi aarch64
* **128** macOS aarch64 (Apple M-series chips)
* **256** Windows x86_64

```{note}
This is a read-only cvar and should not be set by server administrators. ETJump currently supports the following platforms:

* Windows x86
* Linux x86
* Linux x86_64
* macOS x86_64
* macOS aarch64 (Apple M-series chips)
* Windows x86_64
```

---

## g_portalDebug
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_portalDebug           | 0 or 1        | 0

Toggles drawing of portal activation boxes.

---

## g_portalMode
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_portalMode            | 0 or 1        | 1

Toggles restricted portalgun mode. 

* **0** players spawn with a portalgun on every map 
* **1** players don't spawn with a portal gun.

```{note}
This can be overridden on per-map basis with the `portalgun_spawn` [`worldspawn key`](../mapping/mapping_entities.md/#worldspawn).
```

---

## g_rtvMaxMaps
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_rtvMaxMaps            | 2 - 9         | 5

Sets the amount of maps to include in a Rock The Vote.

---

## g_save
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_save                  | 0 or 1        | 1

Toggles players access to [`save`](../client/client_commands.md/#save) and [`load`](../client/client_commands.md/#load).

---

## g_spectatorVote
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_spectatorVote         | 0 - 2         | 0

Sets options for spectators to participate in voting.

* **0** default, spectators cannot participate in voting.
* **1** spectators can cast votes.
* **2** spectators can also call votes.

```{hint}
Only spectators who participate in voting are taken into account by `vote_percent` cvar. This is to prevent votes never passing on servers with multiple idle spectators.
```

---

## g_timerunsDatabase
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_timerunsDatabase      | filename      | timeruns.db

File to store old timerun records in.

```{note}
As of ETJump 3.0.0, this is no longer used to store any timerun records. It is only used to migrate records from old timerun database schema to the new one. New timerun records are saved into the file specified [`g_timeruns2Database`](server_cvars.md/#g_timeruns2database)
```

---

## g_timeruns2Database
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_timeruns2Database     | filename      | timeruns.v2.db

File to store new timerun records in.

---

## g_tokensMode
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_tokensMode            | 0 or 1        | 1

Enables players to use [`!tokens`](admin_system.md/#tokens) command to add collectible tokens into a map. 

---

## g_tokensPath
Name                    | Values         | Default
:-----------------------|:---------------|:------------
g_tokensPath            | directory name | tokens

Directory where tokens information is stored.

---

## g_userConfig
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_userConfig            | filename      | users.db

File to store the user database in.

---

## g_voteCooldown
Name                    | Values               | Default
:-----------------------|:---------------------|:------------
g_voteCooldown          | any positive integer | 15

How long in seconds a player must wait after their previous vote to call another one.

---

## g_weapons
Name                    | Values        | Default
:-----------------------|:--------------|:------------
g_weapons               | 0 or 1        | 1

Toggles whether players spawn with weapons or just knife.

---

## vote_allow_autoRtv
Name                    | Values        | Default
:-----------------------|:--------------|:------------
vote_allow_rtv          | 0 or 1        | 1

Toggles whether players can vote for changing the interval of automatic Rock The Vote.

---

## vote_allow_randommap
Name                    | Values        | Default
:-----------------------|:--------------|:------------
vote_allow_randommap    | 0 or 1        | 1

Toggles whether players can vote for a random map.

---

## vote_allow_rtv
Name                    | Values        | Default
:-----------------------|:--------------|:------------
vote_allow_rtv          | 0 or 1        | 1

Toggles whether players can vote for Rock The Vote.

---

## vote_minRtvDuration
Name                    | Values        | Default
:-----------------------|:--------------|:------------
vote_minRtvDuration     | 1000 - 29000  | 15000

Minimum time in milliseconds Rock The Vote must active before passing.

---

## vote_minVoteDuration
Name                    | Values        | Default
:-----------------------|:--------------|:------------
vote_minVoteDuration    | 1000 - 29000  | 5000

Minimum time in milliseconds a vote must active before passing.
