Here is a list of all currently available commands and their permissions.

## Commands
- [`/snpc help`](#snpc-help)
- [`/snpc set <player> <id>`](#snpc-set-player-id)
- [`/snpc remove <player>`](#snpc-remove-player)
- [`/snpc list`](#snpc-list)

### `/snpc help`
**Permission**: `statusnpc.command.help`

Displays all available commands of the plugin.

----
### /snpc set <player\> <id\>
**Permission**: `statusnpc.command.set`

Links the provided player with the provided NPC (id).

!!! warning "Important"
    - The NPC has to be of the type Player.
    - The player has to be online! (Spigot limitation)

----
### /snpc remove <player\>
**Permission**: `statusnpc.command.remove`

Removes the Player from the npcs.yml file, if linked.

!!! warning "Important"
    - The player has to be online! (Spigot limitation)

----
### `/snpc list`
**Permission**: `statusnpc.command.list`

Lists all currently linked NPC.  
The list contains hover text with additional information.
