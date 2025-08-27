# Portfolio Showcase: TAB Plugin Customization & Scoreboards

Demonstrates applied backend and user-interface skills using the TAB Minecraft plugin. This project highlights my creation of custom scoreboards, tab prefixes, and headers/footers to improve player distinction, real-time server visibility, and user experience.

# Notes

The AFTER section shows all edits I made to the default configuration. Highlights include:
- Custom headers and footers for network-wide consistency
- Dynamic scoreboards displaying player stats, ranks, and server info using placeholders
- Role-based tab and tag prefixes for the Hub, KitPvP, and Survival servers
- Enhanced player visibility and distinction in-game
- Backend-friendly, scalable configuration for multiple servers and roles

```yaml
# BEFORE: Default configuration, no custom headers, footers, or scoreboards

header-footer:
  enabled: true
  header:
    - "<#FFFFFF>&m                                                </#FFFF00>"
    - "&3&lServer name"
    - "&7&l>> %animation:Welcome%&3 &l%player%&7&l! &7&l<<"
    - "&7Online players: &f%online%"
    - "&6Online staff: &e%staffonline%"
    - ""
  footer:
    - "%animation:time%"
    - "&2Ping: %ping%"
    - "&7&l Used memory: %memory-used% MB / %memory-max% MB"
    - ""
    - "&7Visit our webpage %animation:web%"
    - "<#FFFFFF>&m                                                </#FFFF00>"

  scoreboards:
    scoreboard-1.20.3+:
      title: "<#E0B11E>MyServer</#FF0000>"
      display-condition: "%player-version-id%>=765;%bedrock%=false" # Only display it to players using 1.20.3+ AND NOT bedrock edition
      lines:
        - "&7%date%"
        - "%animation:MyAnimation1%"
        - "&6Online:"
        - "* &eOnline&7:||%online%"
        - "* &eCurrent World&7:||%worldonline%"
        - "* &eStaff&7:||%staffonline%"
        - ""
        - "&6Personal Info:"
        - "* &bRank&7:||%group%"
        - "* &bPing&7:||%ping%&8ms"
        - "* &bWorld&7:||%world%"
        - "%animation:MyAnimation1%"

# Default tab prefixes
Player:
  tabprefix: "&0&l[&7&lPlayer&0&l] &3"
  tagprefix: "&2&lPlayer &3"

# AFTER: My Customized Configuration

# Custom Headers & Footers
header-footer:
  enabled: true
  header:
    - '&aSykekeCraft Network &8» &eMain Lobby'
  footer:
    - '&3Connected: &b%online%'

# Custom Scoreboards

# Main Lobby Scoreboard
scoreboards:
  default:
    title: ' &e&lMAIN LOBBY'
    lines:
      - ''
      - '&fPlayer: &6%player%'
      - ''
      - '&fNetwork Online: &a%bungee_total%'
      - ''
      - '&eServers:'
      - '&fMain: &a%bungee_main%'
      - '&fArcade: &a%bungee_arcade%'
      - '&fCreative: &a%bungee_creative%'
      - '&fKitPvP: &a%bungee_kitpvp%'
      - '&fSurvival: &a%bungee_survival%'

  # KitPvP Server Scoreboard
  kitpvp:
    title: '&e&lKITPVP'
    lines:
      - ''
      - '&fPlayer: &6%player%'
      - ''
      - '&fRank: %prisonranksx_currentrank_displayname%'
      - '&fCoins: &a%vault_eco_balance%'
      - '&fKills: &a%statistic_player_kills%'
      - '&fDeaths: &a%statistic_deaths%'
      - '&fServer: &a%online%'
      - '&fNetwork: &a%bungee_total%'

  # Survival Server Scoreboard
  survival:
    title: '&e&lSURVIVAL (SMP)'
    lines:
      - ''
      - '&fPlayer: &6%player%'
      - ''
      - '&fRank: &a%prisonranksx_currentrank_displayname%'
      - '&fCoins: &a%vault_eco_balance%'
      - '&fKills: &a%statistic_player_kills%'
      - '&fDeaths: &a%statistic_deaths%'
      - '&fServer: &a%online%'
      - '&fNetwork: &a%bungee_total%'
