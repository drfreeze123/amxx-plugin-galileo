
---

# Description #

> Nominations can be used to let players nominate maps they would like included in the next map vote. Depending on how many maps have been nominated, it is possible that not all nominations will make it into the next vote.


---

# Related CVARs #

> ## gal\_nom\_playerallowance _<_<sub><a href='cvarNotations.md'>i</a></sub>nominationCount>_##
> Specifies how many nominations each player can make._

> A value of "**0**" will disable this feature.

> Default value is "**2**".

> There is a cap defined by the "MAX\_NOMINATION\_CNT" constant in the SMA. It is set to "**5**" by default. It's not recommended but it can be safely changed if needed. The value of this CVAR needs to be less than or equal to the value of "MAX\_NOMINATION\_CNT".

> ## gal\_nom\_mapfile _<_<sub><a href='cvarNotations.md'>c</a></sub>filename>_##
> Specifies the file to use which holds the names of the maps, listed one per line, that players can nominate._

> Use an asterisk to allow all maps in the server's maps folder to be nominatable instead of setting this value to the name of a file.

> When set to a filename without a path, it assumes the file is in the gamemod folder (i.e. **"cstrike/mapcycle.txt"**).  You can specify a relative path from your gamemod folder before the filename to use files located elsewhere (i.e. **"/addons/amxmodx/configs/mapcycle.txt"**).

> Default value is **"mapcycle.txt"**.

> ## gal\_nom\_prefixes _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##
> Indicates if the **./amxmodx/configs/galileo/[prefixes.ini](filePrefixes_ini.md)** file should be used to attempt to match map names if the player's entered text doesn't match any.
```
0 - do not use prefixes to help match map names
1 - use prefixes to help match names
```
> Default value is "**0**"._

> Setting this to "**1**" can result in lag when players chat (_say_ and _say\_team_) a lot.

> ## gal\_nom\_qtyused _<_<sub><a href='cvarNotations.md'>i</a></sub>nominationCount>_##
> Specifies how many of the nominations made will be considered for use in the next map vote._

> A value of "**0**" means all the nominated maps will be considered.

> Default value is "**0**".


---

# Related Say Commands #

> ## nominate _<_<sub><a href='cvarNotations.md'>c</a></sub>partialMapName>_| nom_<<sub><a href='cvarNotations.md'>c</a></sub>partialMapName>_##
> Attempts to nominate the map specified by_partialMapName_._

> If there are multiple matches for _partialMapName_, a menu of the matches will be displayed to the player allowing them to select map they meant.

> Requires "**gal\_nom\_playerallowance**" to be set to a value higher than "**0**" or the command will not be available.

> ## cancel _<_<sub><a href='cvarNotations.md'>c</a></sub>mapName>_##
> Cancels the nomination of_mapName_, which would have had to be previously nominated by the player._

> Requires "**gal\_nom\_playerallowance**" to be set to a value higher than "**0**" or the command will not be available.

> ## _<_<sub><a href='cvarNotations.md'>c</a></sub>mapName>_##_

> If _mapName_ has been nominated by the player, will cancel the nomination. If _mapname_ has not been nominated by anyone, will attempt to nominate it.

> Requires "**gal\_nom\_playerallowance**" to be set to a value higher than "**0**" or the command will not be available.

> ## nominations | noms ##
> Displays a listing of maps that have been nominated to all players.