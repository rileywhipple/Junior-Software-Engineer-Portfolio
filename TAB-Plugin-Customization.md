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
# Default configuration, no custom headers, footers, or scoreboards
header-footer:
  enabled: false

scoreboards:
  default:
    title: 'Default'
    lines:
      - '{DISPLAYNAME}: {MESSAGE}'

# Default tab prefixes
Default:
  tabprefix: '&7'
  tagprefix: '&7'

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
