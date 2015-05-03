# Description #
> You may have a lot of maps but only a few are sure to attract a lot of players. When the server is empty, you may want the server to change to those maps.

# Related CVARs #

> ## gal\_emptyserver\_wait _<_<sub><a href='cvarNotations.md'>i</a></sub>minutes>_##
> Specifies how many minutes to wait when the server is empty before changing to an alternate empty-server map cycle._

> A value of "**0**" will disable this feature.

> Default value is "**0**".

> ## gal\_emptyserver\_mapfile _<_<sub><a href='cvarNotations.md'>c</a></sub>filename>_##
> Specifies the file which contains a listing of maps, one per line, to be used as the map cycle when the server is empty._

> When set to a filename without a path, it assumes the file is in the game mod folder (i.e. **"cstrike/mapcycle.txt"**). You can specify a relative path from your game mod folder before the filename to use files located elsewhere (i.e. **"/addons/amxmodx/configs/mapcycle.txt"**).

> Default value is **"emptycycle.txt"**.