Most recent changes are at the top.

---


# unreleased | v1.2.xxx #

  * Fixed [issue #13](http://code.google.com/p/amxx-plugin-galileo/issues/detail?id=13); current map in map cycle wasn't being respected in specific cases.
  * Fixed [issue #46](http://code.google.com/p/amxx-plugin-galileo/issues/detail?id=46); incorrect examples were given for folders.
  * Fixed [issue #34](http://code.google.com/p/amxx-plugin-galileo/issues/detail?id=34); when time remaining for a vote is at 0, you can hit a 'voting' key and it shows the time at -1.
  * Fixed [issue #18](http://code.google.com/p/amxx-plugin-galileo/issues/detail?id=18); 'index out of bounds' error if _gal\_ban\_recent_ is set greater than 16. Will cap the maximum maps to ban at the lesser of gal\_ban\_recent or of the MAX\_RECENT\_MAP\_CNT constant.
  * Fixed "invalid cellvector handle provided" error when nominating maps.
  * Removed the need to include "`[`groups`]`" as the very first line when using a "groups" file.
  * Added _gal\_mapfilestyle_ CVAR to indicate the style of the file specified by _gal\_mapfile_.
```
1 - maps file: one map per line, without the ".bsp" extensions
2 - groups file: quantity of maps for each group, on separate lines (groups will be filled in order listed)
3 - groups file: quantity of maps for each group, on separate lines (groups will be filled in random order, not as listed)
```
  * Added ability to disable the "RTV" feature when an admin is present.
```
LANG FILE ADDITION
GAL_ROCK_FAIL_ADMINPRESENT = The "rock the vote" feature is disabled when an admin is present.
```
  * New CVAR, _rtv\_disableFlags_, to indicate if the "rock the vote" feature is disabled while players with the specified standard access flags are in game.
  * Fixed error that occurred when "listmaps" was called and no maps could be nominated.
```
LANG FILE ADDITION
GAL_LISTMAPS_NOMAPS = There are no maps available to be nominated.
```
  * Added 0-byte files into otherwise empty **/data/galileo** folder that are normally created by Galileo later so that admins don't think the folder should be deleted.
  * Fixed error that occurred when "listmaps" was called and no maps could be nominated.
  * Fixed incorrect registered CVAR value for _gal\_nom\_mapfile_ by changing "mapcycle" to "mapcycle.txt".
  * Changed method of specifying a "groups" file and added an option to randomize the order in which the contents of a "groups" file is read.
  * Added referenced, but missing, color code for grey.

# 2009-02-26 | v1.1.290 #

  * Added a check for valid map when populating the various map listings from map list files.
  * Fixed error whem empty server map file doesn't exist.
  * Fixed issue whereas Galileo would set the time limit to 0 in the course of it's regular activities but then sometimes not reset it to the original time limit afterwards.
  * No longer tries to print menus in color if the game mod doesn't support colored menus.
  * Fixed possible RTV exploit by introducing a delay before a single player can RTV after a map change. It's the lesser of either 2 minutes or the value of _gal\_rtv\_wait_.
  * Added additional information to comments for_gal\_nom\_mapfile_,_gal\_vote\_mapfile_, and _gal\_emptyserver\_mapfile_ in **galileo.cfg**.
  * Changed default for _gal\_nom\_prefixes_ from 1 to 0. In other words, the prefix functionality will be turned off by default.
  * Will no longer overwrite an existing menu. This means if a player has another menu open when the map vote starts, they won't see the map vote until the other menu is closed. It also means that, after a player voted and if the server is showing the vote progress, if another menu overwrites Galileo's, the progress won't be shown again until the other menu has been closed. This only affects people that show the in-progress vote status.
  * Now obeys a setting of "0" for _gal\_endofmapvote_. Would previously erroneously present a vote regardless of the setting.
  * New CVAR, _gal\_sounds\_mute_, to indicate if any of the sentences spoken during various events are muted. See **galileo.cfg** for more information.
  * Added code to handle automated version info from SVN. This is of no consequence to anyone but me really, but I wanted to include it in the change log since it actually involves a change to the code.
  * Removed benign code that was prepped for feature utilizing standard maps of each mod. There is no longer any plans to add any information regarding standard maps as I see no use for it.
  * Removed the following language keys:
```
GAL_STANDARD_NOTFOUND
GAL_STANDARD_TOOMANY
GAL_STANDARD_UNKNOWNMOD
```
  * Fixed the "vote filler groups" feature that was previously working incorrectly.

# 2008-09-12 | v1.0.255 #

  * Initial release.