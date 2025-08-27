# Portfolio Showcase: BungeeCord Multi-Server Network

Demonstrates applied backend/network skills on a multi-server Minecraft network.  
This project highlights my edits and configuration enhancements on a default BungeeCord `config.yml`.

---

## Notes
- The **AFTER** section shows all edits I made to the default configuration.
- Highlights include:
  - Network setup & backend server connections
  - Custom MOTDs to enhance user experience
  - Scalable max player and tab size configuration
  - Role-based permissions for users, mods, admins, and owners

---

## Configuration: BEFORE & AFTER

```yaml
# BEFORE: Default auto-generated config (simplified)
servers:
  lobby:
    motd: '&1Just another BungeeCord - Forced Host'
    address: localhost:25565
    restricted: false

listeners:
  - query_port: 25577
    motd: '&1Another Bungee server'

priorities:
  - lobby

bind_local_address: true
host: 0.0.0.0:25577
max_players: 1
tab_size: 60
force_default_server: false

permissions:
  default:
    - bungeecord.command.server
    - bungeecord.command.list
  admin:
    - bungeecord.command.alert
    - bungeecord.command.alertraw
    - bungeecord.command.end
    - bungeecord.command.ip
    - bungeecord.command.reload
    - bungeecord.command.kick
    - bungeecord.command.send
    - bungeecord.command.find
    - bungeecord.command.perms

# AFTER: My Customized Configuration
servers:
  Hub:
    motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'
    address: 169.150.134.43:26910
    restricted: false
  Creative:
    motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'
    address: 173.240.151.92:28824
    restricted: false
  Arcade:
    motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'
    address: 173.240.158.23:25567
    restricted: false
  KitPvP:
    motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'
    address: 173.240.154.7:25580
    restricted: false
  Survival:
    motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'
    address: 173.240.154.116:25579
    restricted: false

listeners:
  query_port: 25565
  motd: '&aTeacher Riley''s Server &f[1.21-1.21.8] &bARCADE &8| &6SURVIVAL &8| &dCREATIVE &8| &cKITPVP'

priorities:
  - Hub
bind_local_address: true
host: 142.79.47.155:25565
max_players: 15
tab_size: 500
force_default_server: true

permissions:
  default:
  - bungeecord.command.server
  - bungeecord.command.list
  mod:
  - staffchat.talk
  - staffchat.read
  - staffchat.join
  - staffchat.leave
  - staffchat.toggle
  - ab.kick.use
  - ab.notify.kick
  - ab.ban.perma
  - ab.ban.temp
  - ab.ban.undo
  - ab.notify.ban
  - ab.notify.tempban
  - ab.ipban.perma
  - ab.ipban.temp
  - ab.notify.ipban
  - ab.notify.tempipban
  - ab.mute.perma
  - ab.mute.temp
  - ab.mute.undo
  - ab.mute.exempt
  - ab.notify.mute
  - ab.tempmute.exempt
  - ab.notify.tempmute
  - ab.warn.perma
  - ab.warn.temp
  - ab.warn.undo
  - ab.notify.warn
  - ab.notify.tempwarn
  - ab.all.undo
  - ab.warns.own
  - ab.warns.other
  - ab.check
  - ab.check.ip
  - ab.changeReason
  - ab.banlist
  - ab.history
  - ab.help
  - bungeecord.command.alert
  - bungeecord.command.find
  - bungeecord.command.send
  admin:
  - staffchat.talk
  - staffchat.read
  - staffchat.join
  - staffchat.leave
  - staffchat.toggle
  - ab.kick.use
  - ab.kick.exempt
  - ab.notify.kick
  - ab.ban.perma
  - ab.ban.temp
  - ab.ban.undo
  - ab.notify.ban
  - ab.notify.tempban
  - ab.ipban.perma
  - ab.ipban.temp
  - ab.notify.ipban
  - ab.notify.tempipban
  - ab.mute.perma
  - ab.mute.temp
  - ab.mute.undo
  - ab.mute.exempt
  - ab.notify.mute
  - ab.tempmute.exempt
  - ab.notify.tempmute
  - ab.warn.perma
  - ab.warn.temp
  - ab.warn.undo
  - ab.warn.exempt
  - ab.notify.warn
  - ab.tempwarn.exempt
  - ab.notify.tempwarn
  - ab.all.undo
  - ab.warns.own
  - ab.warns.other
  - ab.check
  - ab.check.ip
  - ab.changeReason
  - ab.banlist
  - ab.history
  - ab.help
  - bungeecord.command.alert
  - bungeecord.command.end
  - bungeecord.command.reload
  - bungeecord.command.find
  - bungeecord.command.send
  owner:
  - ab.kick.use
  - ab.kick.exempt
  - ab.notify.kick
  - ab.ban.perma
  - ab.ban.temp
  - ab.ban.undo
  - ab.ban.exempt
  - ab.notify.ban
  - ab.tempban.exempt
  - ab.notify.tempban
  - ab.ipban.perma
  - ab.ipban.temp
  - ab.ipban.exempt
  - ab.notify.ipban
  - ab.tempipban.exempt
  - ab.notify.tempipban
  - ab.mute.perma
  - ab.mute.temp
  - ab.mute.undo
  - ab.mute.exempt
  - ab.notify.mute
  - ab.tempmute.exempt
  - ab.notify.tempmute
  - ab.warn.perma
  - ab.warn.temp
  - ab.warn.undo
  - ab.warn.exempt
  - ab.notify.warn
  - ab.tempwarn.exempt
  - ab.notify.tempwarn
  - ab.all.undo
  - ab.warns.own
  - ab.warns.other
  - ab.check
  - ab.check.ip
  - ab.changeReason
  - ab.banlist
  - ab.history
  - ab.reload
  - ab.help
  - ab.systemprefs
  - bungeecord.command.alert
  - bungeecord.command.end
  - bungeecord.command.ip
  - bungeecord.command.reload
  - bungeecord.command.find
  - bungeecord.command.send
