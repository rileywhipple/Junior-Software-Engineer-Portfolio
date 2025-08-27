

# BEFORE: Default chat format (simplified)
format: '&e{DISPLAYNAME}: &f{MESSAGE}'

# Alternative format
# format: '&7[{GROUP}]&r {DISPLAYNAME}&7:&r {MESSAGE}'

# Group-formats not customized
group-formats:
  Default: '{DISPLAYNAME}: {MESSAGE}'

# AFTER: My Customized Configuration

# Default chat format
format: '&e{DISPLAYNAME}: &f{MESSAGE}'

# Custom group chat formats
group-formats:
  Default:       '&8| &7Player &8| &7{DISPLAYNAME} &8» &f{MESSAGE}'
  Player_Blue:   '&8| &3Player &8| &b{DISPLAYNAME} &8» &f{MESSAGE}'
  Player_Red:    '&8| &4Player &8| &c{DISPLAYNAME} &8» &f{MESSAGE}'
  Player_Green:  '&8| &2Player &8| &a{DISPLAYNAME} &8» &f{MESSAGE}'
  Player_Yellow: '&8| &6Player &8| &e{DISPLAYNAME} &8» &f{MESSAGE}'
  Player_Purple: '&8| &5Player &8| &d{DISPLAYNAME} &8» &f{MESSAGE}'
  Trusted:       '&8| &3Trusted &8| &b{DISPLAYNAME} &8» &f{MESSAGE}'
  Friend:        '&8| &dFriend &8| &5{DISPLAYNAME} &8» &f{DISPLAYNAME}'
  Admin:         '&8| &cAdmin &8| &4{DISPLAYNAME} &8» &c{DISPLAYNAME}'
  Owner:         '&8| &bOwner &8| &a{DISPLAYNAME} &8» &f{DISPLAYNAME}'
