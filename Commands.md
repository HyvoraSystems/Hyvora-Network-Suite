# Commands.md

This file lists all known commands from the included Hyvora plugin projects.

---

## HyvoraManager

Platform: **Spigot/Paper**

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/hyvora reload` | `/hnetwork reload`, `/network reload` | Reloads HyvoraManager configuration | `hyvora.reload` |

---

## HyvoraNetworkControl

### Proxy commands

Platform: **BungeeCord**

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/announce <message>` | `/bcannounce` | Broadcasts a network announcement | `hyvora.announce` |
| `/maintenance global <on\|off> [reason]` | `/wartung global <on\|off> [reason]` | Enables/disables global maintenance | `hyvora.maintenance.admin` |
| `/maintenance server <on\|off> <server> [reason]` | `/wartung server <on\|off> <server> [reason]` | Enables/disables maintenance for a single server | `hyvora.maintenance.admin` |
| `/join <server>` | — | Sends the player to another server | `hyvora.join` |
| `/joinme` | — | Sends a clickable JoinMe broadcast | `hyvora.joinme` |
| `/motd <1\|2> <message>` | — | Updates MOTD line 1 or 2 | `hyvora.motd.admin` |
| `/hncreload` | — | Reloads HyvoraNetworkControl | `hyvora.reload` |

### Spigot bridge command

Platform: **Spigot/Paper**

| Command | Description | Permission |
|---|---|---|
| `/network` | Shows HyvoraNetworkControl bridge information | None listed in plugin.yml |

---

## HyvoraNexusCore

Platform: **Spigot/Paper**

| Command | Description | Permission |
|---|---|---|
| `/coins` | Shows your wallet coins | `hyvora.nexus.coins` |
| `/pay <player> <amount>` | Pays coins to another player | `hyvora.nexus.pay` |
| `/bank` | Opens the bank GUI | `hyvora.nexus.bank` |
| `/bank deposit <amount\|all>` | Deposits coins into the bank | `hyvora.nexus.bank.deposit` |
| `/bank withdraw <amount\|all>` | Withdraws coins from the bank | `hyvora.nexus.bank.withdraw` |
| `/bank pay <player> <amount>` | Pays another player from bank balance | `hyvora.nexus.bank.pay` |
| `/bank top` | Opens bank leaderboard | `hyvora.nexus.bank` |
| `/bank history` | Opens bank transaction history | `hyvora.nexus.bank.history` |
| `/bank upgrade` | Attempts to upgrade the bank level | `hyvora.nexus.bank` |
| `/top <level\|coins\|bank\|prestige>` | Opens network leaderboards | `hyvora.nexus.top` |
| `/level` | Opens your level menu | `hyvora.nexus.level` |
| `/level <player>` | Shows another player’s level info | `hyvora.nexus.level` |
| `/prestige` | Performs prestige if possible | `hyvora.nexus.prestige` |
| `/profile` | Opens your profile GUI | `hyvora.nexus.profile` |
| `/achievements` | Opens achievements GUI | `hyvora.nexus.achievements` |
| `/rewards` | Opens rewards GUI | `hyvora.nexus.level` |
| `/nexus` | Shows NexusCore info | None directly; subcommands have permissions |
| `/nexus reload` | Reloads configs | `hyvora.nexus.admin.reload` |
| `/nexus admin` | Opens admin GUI | `hyvora.nexus.admin.gui` |
| `/nexus reset <player>` | Resets a player’s NexusCore data | `hyvora.nexus.admin.reset` |
| `/eco give <player> <amount>` | Gives coins to a player | `hyvora.nexus.admin.eco.give` |
| `/eco take <player> <amount>` | Takes coins from a player | `hyvora.nexus.admin.eco.take` |
| `/eco set <player> <amount>` | Sets a player’s coins | `hyvora.nexus.admin.eco.set` |
| `/coinrain start <seconds> <amount>` | Starts a coin rain event | `hyvora.nexus.admin.coinrain` |
| `/booster start xp <multiplier> <minutes>` | Starts a global XP booster | `hyvora.nexus.admin` |
| `/booster start coins <multiplier> <minutes>` | Starts a global coin booster | `hyvora.nexus.admin` |

---

## HyvoraProxyBanSystem

### Proxy punishment commands

Platform: **BungeeCord**

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/warn <player> <template>` | `/hwarn` | Warns a player using a template | `hyvora.proxyban.warn` |
| `/kick <player> <template>` | `/hkick` | Kicks a player using a template | `hyvora.proxyban.kick` |
| `/mute <player> <template>` | `/hmute` | Mutes a player using a template | `hyvora.proxyban.mute` |
| `/ban <player> <template>` | `/hban` | Bans a player using a template | `hyvora.proxyban.ban` |
| `/unmute <player> <reason>` | — | Removes an active mute | `hyvora.proxyban.unmute` |
| `/unban <player> <reason>` | — | Removes an active ban | `hyvora.proxyban.unban` |

### Spigot GUI commands

Platform: **Spigot/Paper**

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/warns` | — | Opens warn overview GUI | `hyvora.proxyban.gui.warns` |
| `/warns <player>` | — | Opens warn overview filtered by player | `hyvora.proxyban.gui.warns` |
| `/bans` | — | Opens ban overview GUI | `hyvora.proxyban.gui.bans` |
| `/bans <player>` | — | Opens ban overview filtered by player | `hyvora.proxyban.gui.bans` |
| `/punishhistory <player>` | `/phistory`, `/punishmenthistory` | Opens full punishment history GUI | `hyvora.proxyban.gui.history` |
| `/staffstats` | `/punishstats`, `/pbstats` | Opens staff punishment statistics GUI | `hyvora.proxyban.gui.staffstats` |
| `/staffstats <staff>` | `/punishstats <staff>`, `/pbstats <staff>` | Filters staff statistics by staff name | `hyvora.proxyban.gui.staffstats` |

---

## NexusSocial: Eternal Bonds

### Spigot/Paper commands

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/nexus` | — | Opens the NexusSocial main menu | `nexussocial.command.nexus` |
| `/friends` | `/friendlist`, `/fl` | Opens the friends menu | `nexussocial.command.friends` |
| `/friend` | — | Opens the friends menu | `nexussocial.command.friend` |
| `/friend add <player>` | — | Sends a friend request | `nexussocial.command.friend` |
| `/friend accept [player]` | — | Accepts a friend request | `nexussocial.command.friend` |
| `/friend deny [player]` | `/friend decline [player]` | Denies a friend request | `nexussocial.command.friend` |
| `/friend requests` | — | Opens friend requests GUI | `nexussocial.command.friend` |
| `/friend toggle` | — | Enables/disables incoming friend requests | `nexussocial.command.friend` |
| `/friend best <player>` | `/friend soulbond <player>` | Toggles best friend / soulbond | `nexussocial.command.friend` |
| `/friend remove <player>` | — | Removes a friend | `nexussocial.command.friend` |
| `/friend block <player>` | — | Blocks a player | `nexussocial.command.friend` |
| `/friend unblock <player>` | — | Unblocks a player | `nexussocial.command.friend` |
| `/friend tp <player>` | `/friend teleport <player>` | Teleports to a friend where supported | `nexussocial.command.friend` |
| `/friend msg <player> <message>` | `/friend message <player> <message>` | Starts or sends a friend message flow | `nexussocial.command.friend` |
| `/friend memory <player> <text>` | `/friend note <player> <text>` | Saves a friend memory/note | `nexussocial.command.friend` |
| `/friend profile <player>` | `/friend story <player>` | Opens a friend profile | `nexussocial.command.friend` |

### Party commands

| Command | Alias | Description | Permission |
|---|---|---|---|
| `/party` | — | Opens/creates the party menu | `nexussocial.command.party` |
| `/party create` | — | Creates a party | `nexussocial.command.party` |
| `/party invite <player>` | — | Invites a player | `nexussocial.command.party` |
| `/party accept [player]` | — | Accepts a party invite | `nexussocial.command.party` |
| `/party deny [player]` | `/party decline [player]` | Denies a party invite | `nexussocial.command.party` |
| `/party invites` | — | Opens party invite GUI | `nexussocial.command.party` |
| `/party join <leader>` | — | Joins a public or available party | `nexussocial.command.party` |
| `/party leave` | `/party disband` | Leaves or disbands the party | `nexussocial.command.party` |
| `/party ready` | — | Toggles ready state | `nexussocial.command.party` |
| `/party role <TANK\|HEALER\|DPS\|SUPPORT>` | — | Sets your party role | `nexussocial.command.party` |
| `/party kick <player>` | — | Kicks a party member | `nexussocial.party.kick` |
| `/party transfer <player>` | — | Transfers party leadership | `nexussocial.party.transfer` |
| `/party rename <name>` | — | Renames the party | `nexussocial.command.party` |
| `/party public` | — | Toggles public party mode | `nexussocial.mythic.publicparty` |
| `/party list` | — | Lists public parties | `nexussocial.command.party` |
| `/party chat` | — | Toggles party chat mode | `nexussocial.command.party` |
| `/party status` | — | Shows party status | `nexussocial.command.party` |

### Clan commands

| Command | Description | Permission |
|---|---|---|
| `/clan` | Opens clan menu | `nexussocial.command.clan` |
| `/clan create <tag> <name>` | Creates a clan | `nexussocial.command.clan` |
| `/clan invite <player>` | Invites a player to the clan | `nexussocial.clan.invite` |
| `/clan invites` | Opens clan invite GUI | `nexussocial.command.clan` |
| `/clan accept <tag>` | Accepts a clan invite | `nexussocial.command.clan` |
| `/clan deny <tag>` | Denies a clan invite | `nexussocial.command.clan` |
| `/clan leave` | Leaves the clan | `nexussocial.command.clan` |
| `/clan disband` | Disbands the clan | `nexussocial.clan.manage` |
| `/clan kick <player>` | Kicks a clan member | `nexussocial.clan.manage` |
| `/clan promote <player>` | Promotes a clan member | `nexussocial.clan.manage` |
| `/clan demote <player>` | Demotes a clan member | `nexussocial.clan.manage` |
| `/clan transfer <player>` | Transfers clan leadership | `nexussocial.clan.manage` |
| `/clan rename <name>` | Renames the clan | `nexussocial.clan.manage` |
| `/clan tag <tag>` | Changes clan tag | `nexussocial.clan.manage` |
| `/clan deposit <amount>` | Deposits into clan bank | `nexussocial.command.clan` |
| `/clan sethome` | Sets the clan home | `nexussocial.clan.home` |
| `/clan home` | Teleports to clan home | `nexussocial.clan.home` |
| `/clan ally <tag>` | Sets a clan as ally | `nexussocial.clan.relations` |
| `/clan enemy <tag>` | Sets a clan as enemy | `nexussocial.clan.relations` |
| `/clan neutral <tag>` | Sets a clan as neutral | `nexussocial.clan.relations` |
| `/clan war <tag>` | Starts or views clan war interaction | `nexussocial.clan.war` |
| `/clan claim <questId>` | Claims a clan quest reward | `nexussocial.command.clan` |
| `/clan buildings` | Opens clan buildings GUI | `nexussocial.command.clan` |
| `/clan members` | Opens clan members GUI | `nexussocial.command.clan` |
| `/clan quests` | Opens clan quests GUI | `nexussocial.command.clan` |
| `/clan perks` | Opens clan perks GUI | `nexussocial.command.clan` |

### Proxy MSG commands

Platform: **BungeeCord**

| Command | Aliases | Description | Permission |
|---|---|---|---|
| `/msg <player> <message>` | `/tell`, `/w`, `/pm`, `/message` | Sends a cross-server private message | `nexussocial.msg.use` |
| `/r <message>` | `/reply` | Replies to the last private message | `nexussocial.msg.reply` |
| `/msgtoggle` | `/togglemsg`, `/pmtoggle` | Toggles private messages | `nexussocial.msg.toggle` |
| `/msgspy` | `/socialspy` | Toggles message spy | `nexussocial.msg.spy` |
| `/nexussocialproxy status` | `/nsp status` | Shows proxy bridge status | `nexussocial.proxy.admin` |
