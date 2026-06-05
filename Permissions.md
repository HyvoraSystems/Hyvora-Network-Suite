# Permissions.md

This file lists the permissions found in the included Hyvora plugin projects.

---

## HyvoraManager

| Permission | Default | Description |
|---|---:|---|
| `hyvora.admin` | OP | General HyvoraManager admin permission |
| `hyvora.reload` | OP | Allows `/hyvora reload` |
| `hyvora.chat.color` | false | Allows legacy chat colors |
| `hyvora.chat.hex` | false | Allows HEX chat colors |
| `hyvora.tab.admin` | OP | Admin-level TAB related permission |

---

## HyvoraNetworkControl

| Permission | Default | Description |
|---|---:|---|
| `hyvora.announce` | not listed | Allows `/announce` |
| `hyvora.maintenance.admin` | not listed | Allows maintenance commands |
| `hyvora.maintenance.bypass` | config/default | Allows joining during maintenance |
| `hyvora.network.maintenance.bypass` | code fallback | Alternative maintenance bypass checked in code |
| `hyvora.network.bypass` | OP | Spigot bridge bypass permission from plugin.yml |
| `hyvora.join` | not listed | Allows `/join <server>` |
| `hyvora.joinme` | not listed | Allows `/joinme` |
| `hyvora.motd.admin` | not listed | Allows `/motd` |
| `hyvora.reload` | not listed | Allows `/hncreload` |
| `hyvora.admin` | not listed | General network admin permission used by service logic |

**Important:** Proxy permissions must be assigned on the BungeeCord/LuckPerms proxy side.

---

## HyvoraNexusCore

### User permissions

| Permission | Default | Description |
|---|---:|---|
| `hyvora.nexus.level` | true | Allows `/level` and level GUI |
| `hyvora.nexus.coins` | true | Allows `/coins` |
| `hyvora.nexus.pay` | true | Allows `/pay` |
| `hyvora.nexus.bank` | true | Allows `/bank` |
| `hyvora.nexus.bank.deposit` | true | Allows `/bank deposit` |
| `hyvora.nexus.bank.withdraw` | true | Allows `/bank withdraw` |
| `hyvora.nexus.bank.pay` | true | Allows `/bank pay` |
| `hyvora.nexus.bank.history` | true | Allows `/bank history` |
| `hyvora.nexus.top` | true | Allows `/top` |
| `hyvora.nexus.profile` | true | Allows `/profile` |
| `hyvora.nexus.achievements` | true | Allows `/achievements` |
| `hyvora.nexus.prestige` | true | Allows `/prestige` |

### Admin permissions

| Permission | Default | Description |
|---|---:|---|
| `hyvora.nexus.admin` | OP | General NexusCore admin permission |
| `hyvora.nexus.admin.reload` | OP | Allows `/nexus reload` |
| `hyvora.nexus.admin.eco.give` | OP | Allows `/eco give` |
| `hyvora.nexus.admin.eco.take` | OP | Allows `/eco take` |
| `hyvora.nexus.admin.eco.set` | OP | Allows `/eco set` |
| `hyvora.nexus.admin.level.set` | OP | Reserved/admin level set permission |
| `hyvora.nexus.admin.xp.give` | OP | Reserved/admin XP give permission |
| `hyvora.nexus.admin.bank.set` | OP | Reserved/admin bank set permission |
| `hyvora.nexus.admin.reset` | OP | Allows `/nexus reset <player>` |
| `hyvora.nexus.admin.gui` | OP | Allows `/nexus admin` |
| `hyvora.nexus.admin.coinrain` | OP | Allows `/coinrain start` |

---

## HyvoraProxyBanSystem

### Staff action permissions

| Permission | Default | Description |
|---|---:|---|
| `hyvora.proxyban.warn` | not listed | Allows `/warn` |
| `hyvora.proxyban.kick` | not listed | Allows `/kick` |
| `hyvora.proxyban.mute` | not listed | Allows `/mute` |
| `hyvora.proxyban.unmute` | not listed | Allows `/unmute` |
| `hyvora.proxyban.ban` | not listed | Allows `/ban` |
| `hyvora.proxyban.unban` | not listed | Allows `/unban` |
| `hyvora.proxyban.notify` | not listed | Receives staff punishment notifications |

### GUI permissions

| Permission | Default | Description |
|---|---:|---|
| `hyvora.proxyban.gui.warns` | OP | Allows `/warns` |
| `hyvora.proxyban.gui.bans` | OP | Allows `/bans` |
| `hyvora.proxyban.gui.history` | OP | Allows `/punishhistory` |
| `hyvora.proxyban.gui.staffstats` | OP | Allows `/staffstats` |
| `hyvora.proxyban.gui.deletewarn` | OP | Allows deleting warns through GUI |

### Exempt permissions

Players with these permissions cannot be punished by normal staff.

| Permission | Description |
|---|---|
| `hyvora.proxyban.exempt.warn` | Protects from warns |
| `hyvora.proxyban.exempt.kick` | Protects from kicks |
| `hyvora.proxyban.exempt.mute` | Protects from mutes |
| `hyvora.proxyban.exempt.ban` | Protects from bans |

### Override-exempt permissions

Players with these permissions can punish protected players anyway.

| Permission | Description |
|---|---|
| `hyvora.proxyban.overrideexempt.warn` | Allows warning exempt players |
| `hyvora.proxyban.overrideexempt.kick` | Allows kicking exempt players |
| `hyvora.proxyban.overrideexempt.mute` | Allows muting exempt players |
| `hyvora.proxyban.overrideexempt.ban` | Allows banning exempt players |

### Dashboard extra permissions

These are dashboard-level permissions, not Minecraft command permissions.

| Dashboard permission | Description |
|---|---|
| `manage_users` | Create, edit and delete dashboard users |
| `manage_templates` | Create, edit and delete punishment templates |
| `override_exempt` | Bypass exempt protection in dashboard |
| `edit` | Edit punishments in dashboard |
| `remove` | Remove punishments in dashboard |
| `punish_warn` | Warn from dashboard |
| `punish_kick` | Kick from dashboard |
| `punish_mute` | Mute from dashboard |
| `punish_ban` | Ban from dashboard |

---

## NexusSocial: Eternal Bonds

### Basic command permissions

| Permission | Default | Description |
|---|---:|---|
| `nexussocial.command.nexus` | true | Allows `/nexus` |
| `nexussocial.command.friends` | true | Allows `/friends` |
| `nexussocial.command.friend` | true | Allows `/friend` |
| `nexussocial.command.party` | true | Allows `/party` |
| `nexussocial.command.clan` | true | Allows `/clan` |
| `nexussocial.admin.reload` | OP | Allows admin reload from NexusSocial menu/command logic |

### Party permissions

| Permission | Default | Description |
|---|---:|---|
| `nexussocial.vip.party.6` | false | Allows party size up to 6 |
| `nexussocial.mythic.party.10` | false | Allows party size up to 10 |
| `nexussocial.party.size.32` | false | Allows party size up to 32 |
| `nexussocial.mythic.publicparty` | false | Allows public party toggle |
| `nexussocial.party.kick` | true | Allows party kick tools |
| `nexussocial.party.transfer` | true | Allows party leadership transfer |

### Friend permissions

| Permission | Default | Description |
|---|---:|---|
| `nexussocial.friend.block` | true | Allows friend block/unblock features |
| `nexussocial.friend.soulbond` | true | Allows Best Friend/Soulbond features |

### Clan permissions

| Permission | Default | Description |
|---|---:|---|
| `nexussocial.clan.invite` | true | Allows clan invites |
| `nexussocial.clan.manage` | OP | Allows clan management actions |
| `nexussocial.clan.exempt.hopping` | false | Exempts from clan hopping restrictions |
| `nexussocial.clan.home` | true | Allows clan home features |
| `nexussocial.clan.relations` | true | Allows ally/enemy/neutral relation tools |
| `nexussocial.clan.war` | true | Allows clan war tools |

### Proxy MSG permissions

| Permission | Default | Description |
|---|---:|---|
| `nexussocial.msg.use` | proxy command | Allows `/msg` |
| `nexussocial.msg.reply` | proxy command | Allows `/r` |
| `nexussocial.msg.toggle` | proxy command | Allows `/msgtoggle` |
| `nexussocial.msg.spy` | proxy command | Allows `/msgspy` |
| `nexussocial.msg.bypasscooldown` | false | Bypasses MSG cooldown |
| `nexussocial.msg.bypasstoggle` | false | Can message players who disabled messages |
| `nexussocial.proxy.admin` | proxy command | Allows `/nsp status` and proxy admin commands |

---

## Suggested LuckPerms group layout

### Default player

```text
hyvora.nexus.level
hyvora.nexus.coins
hyvora.nexus.pay
hyvora.nexus.bank
hyvora.nexus.bank.deposit
hyvora.nexus.bank.withdraw
hyvora.nexus.bank.pay
hyvora.nexus.bank.history
hyvora.nexus.top
hyvora.nexus.profile
hyvora.nexus.achievements
hyvora.nexus.prestige
nexussocial.command.nexus
nexussocial.command.friends
nexussocial.command.friend
nexussocial.command.party
nexussocial.command.clan
nexussocial.party.kick
nexussocial.party.transfer
nexussocial.friend.block
nexussocial.friend.soulbond
nexussocial.clan.invite
nexussocial.clan.home
nexussocial.clan.relations
nexussocial.clan.war
nexussocial.msg.use
nexussocial.msg.reply
nexussocial.msg.toggle
```

### VIP

```text
nexussocial.vip.party.6
```

### Mythic

```text
nexussocial.mythic.party.10
nexussocial.mythic.publicparty
```

### Staff

```text
hyvora.proxyban.warn
hyvora.proxyban.kick
hyvora.proxyban.mute
hyvora.proxyban.notify
hyvora.proxyban.gui.warns
hyvora.proxyban.gui.bans
hyvora.proxyban.gui.history
hyvora.proxyban.gui.staffstats
```

### Admin

```text
hyvora.admin
hyvora.reload
hyvora.announce
hyvora.maintenance.admin
hyvora.maintenance.bypass
hyvora.join
hyvora.joinme
hyvora.motd.admin
hyvora.nexus.admin
hyvora.nexus.admin.reload
hyvora.nexus.admin.eco.give
hyvora.nexus.admin.eco.take
hyvora.nexus.admin.eco.set
hyvora.nexus.admin.reset
hyvora.nexus.admin.gui
hyvora.nexus.admin.coinrain
hyvora.proxyban.ban
hyvora.proxyban.unban
hyvora.proxyban.unmute
hyvora.proxyban.gui.deletewarn
nexussocial.proxy.admin
nexussocial.msg.spy
```
