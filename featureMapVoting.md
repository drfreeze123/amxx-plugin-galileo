# Description #

> This is what most people generally think of when they think of starting a vote for a new map. It's just a standard map vote.

# Related CVARs #

> ## gal\_vote\_mapchoices _<_<sub><a href='cvarNotations.md'>i</a></sub>mapCount>_##
> Specifies the number of maps players can choose from during the vote._

> The number of maps must be between 2 and 8.

> Default value is "**5**".

> ## gal\_vote\_duration _<_<sub><a href='cvarNotations.md'>i</a></sub>seconds>_##
> Specifies the number of seconds the vote should last._

> Default value is "**15**".

> ## gal\_vote\_mapfile _<_<sub><a href='cvarNotations.md'>c</a></sub>filename>_##
> Specifies the file to use which either holds the names of the maps, one per line, that the vote will be filled with or is used with the [map group feature](featureVoteFillGroups.md) to specify how many maps to use from each group._

> When set to a filename without a path, it assumes the file is in the game mod folder (i.e. **"cstrike/mapcycle.txt"**).  You can specify a relative path from your game mod folder before the filename to use files located elsewhere (i.e. **"/addons/amxmodx/configs/mapcycle.txt"**).

> Default value is **"mapcycle.txt"**.

> ## gal\_vote\_mapfilestyle _<_<sub><a href='cvarNotations.md'>i</a></sub>style>_##
> Indicates how the file specified by "gal\_vote\_mapfile" is setup.
```
1 - maps file: one map per line, without the ".bsp" extensions
2 - groups file: quantity of maps for each group, on separate lines (groups will be filled in order listed)
3 - groups file: quantity of maps for each group, on separate lines (groups will be filled in random order, not as listed)
```
> Default value is "**1**"._

> ## gal\_vote\_uniqueprefixes _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##
> Indicates whether the maps being added, after nominations have been added to a vote, should have unique map prefixes from those already in the vote._

> Default value is "**0**".

> Nominations are exempt from the check for unique prefixes. Nominations are added and then Galileo will start checking the rest of the maps against the maps already added.

> ## gal\_vote\_overwritemenu _<_<sub><a href='cvarNotations.md'>i</a></sub>overwrite>_##
> Indicates whether to overwrite existing menus with the map vote menu.
```
0 - only show vote menu if player isn't already shown a menu
1 - always overwrite existing menus with the vote menu
```
> Default value is "**1**"._

> It is possible that, if set to "0", a player may not have an existing  menu displayed but still won't be shown the map vote menu.

> ## gal\_vote\_announcechoice _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##
> Indicates whether to announce each player's choice.
```
0 - keep the player's choice private
1 - announce the player's choice
```
> Default value is "**1**"._

> When the player's choice is announced, everyone on the server is shown what every other player's selection was.

> ## gal\_vote\_expirationcountdown _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##
> Indicates whether a vote expiration countdown should be displayed.
```
0 - do not show the countdown
1 - show the countdown
```
> Default value is "**1**"._

> The vote expiration countdown will display a timer to players that haven't voted, when there are 10 seconds left in the current vote. The timer counts down from 10 to 0, at which point the vote will be over.

> ## gal\_sounds\_mute _<_<sub><a href='cvarNotations.md'>i</a></sub>flags>_##
> There will be words spoken during certain events to reinforce in a player's mind what is happening. You may choose to mute any that you would rather not have spoken._

> Indicates if any sounds should be muted during the various events in which they'd normal be spoken.

> The flags are additive. A value of **0** will not mute any of the sounds.
```
1 - "get ready to choose a map"
2 - "7, 6, 5, 4, 3, 2, 1"
4 - "time to choose"
8 - "runoff voting is required"
```
> Default value is "**0**".

# Related Console Commands #

> ## gal\_startvote `[`-nochange`]` ##
> Forces a map vote to begin and the map will be changed once the next map has been determined. If the "-nochange" argument is supplied, the map will not be changed by Galileo, which is useful when you have a different plugin handling the actual changing of the map.

> ## gal\_createmapfile _<_<sub>c</sub>filename>