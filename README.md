# MOTDForDys

The MOTD seems to be disabled in Dystopia. This plugin creates the "motd" command to show the MOTD, and will display it automatically when a player enters the server if the "motdfordys_automotd" ConVar is set to 1. This plugin will conflict with the basetriggers plugin that ships with vanilla SourceMod, because they both create the "motd" command. However many of the functions provided by basetriggers do not work properly in Dystopia, and I would recommend removing it. This will probably also work for other games, that the basetriggers motd command would work properly for.

Convar:
```
motdfordys_automotd "<1|0>" Default Value "1"
```

Command:
```
motd
```

Special Credits:

- Vizzy http://steamcommunity.com/profiles/76561197972958598/ \- For testing the plugin.
- SourceMod Development Team \- The implementation of the motd command was basically copied from basetriggers.

Known Bugs:

- It seems that when Dystopia is played at non-native resolutions, a button at the top right corner of the panel is visible, in addition to the normal "OK" button. The top right button will not properly close the MOTD panel. The transparent panel will be visible with no text or buttons, and no apparent way to continue without disconnecting from the server, after closing the loadouts menu with the button labled "Done!". Although, it does seem to close properly if the loadouts menu is closed by joining the Spectators team. This issue is probably with how VGUI panels are handled in Dystopia, and probably cannot be fixed in SourceMod.