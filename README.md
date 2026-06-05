# Hyvora Network Suite

**Hyvora Network Suite** is a modular BungeeCord + Spigot/Paper plugin ecosystem for modern Minecraft networks.  
It combines network management, chat/TAB styling, global economy and progression, punishments, social systems, clans, parties and cross-server private messaging into one clean Hyvora-branded server experience.

The suite is designed for networks that want a premium, consistent, English-only setup with HEX colors, LuckPerms support, PlaceholderAPI integration, MySQL persistence and clickable interactive menus.

---

## Included plugins

| Plugin | Platform | Purpose |
|---|---|---|
| **HyvoraManager** | BungeeCord + Spigot/Paper | Network styling core with chat, TAB, join/quit messages, LuckPerms prefix/suffix support and placeholder bridge |
| **HyvoraNetworkControl** | BungeeCord + Spigot/Paper | Network administration: announcements, maintenance, MOTD, join/joinme, fallback handling and web dashboard |
| **HyvoraNexusCore** | BungeeCord + Spigot/Paper | Global levels, XP, coins, bank, rewards, achievements, prestige, leaderboards and scoreboard |
| **HyvoraProxyBanSystem** | BungeeCord + Spigot/Paper | Network-wide punishments with templates, mutes, bans, warns, history GUIs and dashboard |
| **NexusSocial: Eternal Bonds** | BungeeCord + Spigot/Paper | Friends, parties, clans, social GUIs, PlaceholderAPI placeholders and proxy-wide MSG system |

---

## Full plugin description

### HyvoraManager

HyvoraManager is the visual identity layer of the network. It keeps chat, TAB, prefixes, join messages and quit messages in one consistent Hyvora style.

**Highlights**

- Clean English default configuration
- Modern HEX color support
- Supports `&#RRGGBB`, `#RRGGBB`, `<#RRGGBB>` and `&x&R&R&G&G&B&B`
- LuckPerms prefix, suffix and group integration
- PlaceholderAPI support
- Chat format with hover and click actions
- TAB header/footer with animated premium look
- Rank sorting through LuckPerms group weights
- Clean join and quit messages
- Built-in Hyvora placeholder bridge for server, network, level, coins, bank, clan, party and friends values

This plugin should be installed on every backend server where you want the Hyvora chat/TAB appearance.

---

### HyvoraNetworkControl

HyvoraNetworkControl is the proxy-side control center for the whole network. It manages important network operations directly on BungeeCord and includes a small Spigot bridge.

**Highlights**

- Global announcements
- Global and per-server maintenance mode
- Maintenance bypass permission
- `/join <server>` for quick server switching
- `/joinme` clickable broadcast
- Editable MOTD line 1 and line 2
- HEX MOTD rendering
- Fallback server support
- Custom restart/stop message
- Embedded web dashboard
- MySQL dashboard user system
- HikariCP MySQL connection pool shaded into the proxy jar

The dashboard can be used to control MOTD, maintenance and network state through a browser. For production usage, put it behind HTTPS, firewall or a reverse proxy.

---

### HyvoraNexusCore

HyvoraNexusCore is the global progression and economy core. It stores player data network-wide and provides the base for long-term activity systems.

**Highlights**

- Global XP and level system
- Prestige system
- Coins wallet
- Bank system with deposit, withdraw, bank pay, bank top and history
- Daily login XP and playtime XP
- Server-switch XP from proxy events
- Rewards GUI
- Achievements GUI
- Profile GUI
- Leaderboards
- Coin rain events
- Global XP and coin boosters
- Scoreboard with PlaceholderAPI bridge
- LuckPerms prefix/suffix integration
- MySQL/MariaDB persistence
- HikariCP connection pooling

This plugin is the central player progression layer and is ideal as the main “activity engine” of the network.

---

### HyvoraProxyBanSystem

HyvoraProxyBanSystem provides network-wide punishments through BungeeCord while offering clean Spigot inventory GUIs for staff overview and history management.

**Highlights**

- Proxy-wide warn, kick, mute and ban commands
- Template-based punishment reasons and durations
- Unmute and unban commands
- Network-wide mute listener
- Proxy login ban listener
- Offline UUID support
- Staff notifications
- Auto-ban after configurable warn limit
- Exempt permissions
- Override-exempt permissions
- `/warns` GUI
- `/bans` GUI
- Full punishment history GUI
- Staff statistics GUI
- Warn delete confirmation GUI
- Search and pagination
- Player heads in GUIs
- Built-in web dashboard
- Dashboard roles and users
- Template editing through dashboard, saved into `templates.yml`

The proxy module performs the punishments. The Spigot module provides Bukkit inventory GUIs. Both modules must use the same database.

---

### NexusSocial: Eternal Bonds

NexusSocial is the social layer of the network. It adds friends, requests, friend profiles, parties, clans and a BungeeCord-wide private message system.

**Highlights**

- Friends GUI
- Friend requests
- Accept/deny workflow
- Toggle friend requests on/off
- Friend blocking
- Best Friend / Soulbond system
- Friend memory notes
- Friend teleport
- Friend profile view
- Party creation and invites
- Party ready system
- Party roles: Tank, Healer, DPS, Support
- Party leader tools: kick, transfer, rename
- Party chat toggle
- Public parties
- Party sizes: default 3, VIP 6, Mythic 10, permission hard-cap 32
- Clan creation with tag and name
- Clan invites
- Clan ranks, promote/demote, transfer, kick
- Clan bank deposit
- Clan home
- Clan relations: ally, enemy, neutral
- Clan wars and quests
- Clan buildings and perks GUIs
- Full proxy-side `/msg` system
- Reply, toggle messages and message spy
- PlaceholderAPI placeholders for friends, parties and clans

This plugin makes the network feel alive by adding long-term social progression and interactive menus.

---

## Requirements

| Requirement | Recommended |
|---|---|
| Java | Java 17 or newer |
| Proxy | BungeeCord / Waterfall |
| Backend | Paper / Spigot |
| Database | MySQL or MariaDB |
| Build tool | Maven |
| Optional dependencies | LuckPerms, PlaceholderAPI |

---

## Installation overview

1. Build every project with Maven:
   ```bash
   mvn clean package
   ```

2. Put proxy jars into the BungeeCord `plugins/` folder:
   - HyvoraManager Bungee jar
   - HyvoraNetworkControl Proxy jar
   - HyvoraNexusCore Proxy jar
   - HyvoraProxyBan Proxy jar
   - NexusSocial Proxy jar

3. Put Spigot/Paper jars into every backend server where the feature should work:
   - HyvoraManager Spigot jar
   - HyvoraNetworkControl Spigot bridge jar
   - HyvoraNexusCore Spigot jar
   - HyvoraProxyBanGUI Spigot jar
   - NexusSocial Spigot jar

4. Start proxy and backend servers once.

5. Configure the generated MySQL/MariaDB data in all configs.

6. Restart proxy and backend servers.

7. Install LuckPerms and PlaceholderAPI where needed.

---

## Suggested database layout

You can use separate databases or one shared database with different table prefixes.  
The cleanest setup is:

| Plugin | Suggested database |
|---|---|
| HyvoraNetworkControl | `hyvora_network` |
| HyvoraNexusCore | `hyvora_nexus` |
| HyvoraProxyBanSystem | `hyvora_network` or `hyvora_punishments` |
| NexusSocial | `nexussocial` or `hyvora_social` |

---

## Important LuckPerms setup

For proxy commands and bypass permissions, assign permissions on the proxy context, not only on backend servers.

Example:

```bash
/lpb user <player> permission set hyvora.maintenance.bypass true
/lpb user <player> permission set nexussocial.msg.spy true
/lpb user <player> permission set hyvora.proxyban.ban true
```

For TAB rank sorting, use LuckPerms weights:

```bash
/lp group default setweight 1
/lp group premium setweight 2
/lp group vip setweight 3
/lp group mythic setweight 4
/lp group creator setweight 5
/lp group builder setweight 6
/lp group support setweight 7
/lp group moderator setweight 8
/lp group srmoderator setweight 9
/lp group manager setweight 10
/lp group developer setweight 11
/lp group sradmin setweight 12
/lp group admin setweight 13
```

---

## Placeholder overview

### HyvoraManager internal placeholders

- `%player_name%`
- `%player_displayname%`
- `%hyvora_server%`
- `%hyvora_network%`
- `%hyvora_level%`
- `%hyvora_xp%`
- `%hyvora_xp_needed%`
- `%hyvora_coins%`
- `%hyvora_bank%`
- `%hyvora_clan%`
- `%hyvora_clan_tag%`
- `%hyvora_party%`
- `%hyvora_friends_online%`
- `%server_online%`
- `%server_max_players%`
- `%luckperms_prefix%`
- `%luckperms_suffix%`
- `%luckperms_group%`

### HyvoraNexusCore PlaceholderAPI placeholders

- `%nexus_level%`
- `%nexus_xp%`
- `%nexus_needed_xp%`
- `%nexus_xp_bar%`
- `%nexus_prestige%`
- `%nexus_coins%`
- `%nexus_bank%`
- `%nexus_bank_level%`
- `%nexus_total_earned%`
- `%nexus_total_spent%`
- `%nexus_title%`
- `%nexus_rank_title%`

### NexusSocial PlaceholderAPI placeholders

Friends:

- `%nexus_friends_count%`
- `%nexus_friends_online%`
- `%nexus_friends_offline%`
- `%nexus_friends_requests_incoming%`
- `%nexus_friends_requests_outgoing%`
- `%nexus_friends_best_count%`
- `%nexus_friends_blocked_count%`
- `%nexus_friends_requests_enabled%`
- `%nexus_friendship_level_<player>%`
- `%nexus_social_score%`
- `%nexus_global_social_rank%`

Party:

- `%nexus_party_name%`
- `%nexus_party_size%`
- `%nexus_party_max_size%`
- `%nexus_party_role%`
- `%nexus_party_ready%`
- `%nexus_party_ready_count%`
- `%nexus_party_leader%`
- `%nexus_party_is_leader%`
- `%nexus_party_public%`
- `%nexus_party_pending_invites%`
- `%nexus_party_chat%`
- `%nexus_party_all_ready%`
- `%nexus_party_has_party%`

Clan:

- `%nexus_clan_tag%`
- `%nexus_clan_name%`
- `%nexus_clan_tag_formatted%`
- `%nexus_clan_tier%`
- `%nexus_clan_level%`
- `%nexus_clan_xp%`
- `%nexus_clan_xp_needed%`
- `%nexus_clan_xp_bar%`
- `%nexus_clan_power%`
- `%nexus_clan_bank%`
- `%nexus_clan_members_online%`
- `%nexus_clan_members_total%`
- `%nexus_clan_rank%`
- `%nexus_clan_invites%`
- `%nexus_clan_pending_invites%`
- `%nexus_clan_season_rank%`
- `%nexus_clan_war_status%`
- `%nexus_clan_war_points_own%`
- `%nexus_clan_war_points_enemy%`
- `%nexus_clan_allies%`
- `%nexus_clan_enemies%`
- `%nexus_clan_home_set%`
- `%nexus_clan_building_total_level%`
- `%nexus_clan_quests_completed%`
- `%nexus_clan_has_clan%`
- `%nexus_clan_building_level_<building_name>%`
- `%nexus_clan_quest_progress_<quest_id>%`

---

## Suggested SpigotMC description

**Hyvora Network Suite** is a premium modular Minecraft network system for BungeeCord and Spigot/Paper servers.  
It includes a polished chat/TAB manager, network control tools, MOTD and maintenance management, global economy, levels, bank, rewards, achievements, proxy-wide punishments, staff GUIs, web dashboards, friends, parties, clans and a full cross-server MSG system.

Built for modern networks, Hyvora focuses on clean English messages, HEX gradients, LuckPerms integration, PlaceholderAPI support and MySQL persistence. Every module can be used separately, but together they create a complete and professional server network foundation.

**Main features**

- BungeeCord + Spigot/Paper support
- HEX and gradient styling
- LuckPerms prefixes, suffixes and rank sorting
- PlaceholderAPI support
- Chat, TAB, join and quit styling
- Announcements and clickable JoinMe
- Global and per-server maintenance
- MOTD editor
- Web dashboards
- Global coins, bank, XP and levels
- Prestige, rewards and achievements
- Network-wide punishments
- Warns, bans, history and staff stats GUIs
- Friends, parties and clans
- Cross-server private messages
- MySQL/MariaDB persistence
- English-only default configuration

Perfect for server owners who want a consistent, polished and expandable network core.
