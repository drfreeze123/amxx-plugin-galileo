
---

# Description #

> There are two standard HL1 map related commands that you may not want to function normally, if at all when using this plugin, so as to avoid conflicts of map voting procedures.


---

# Related CVARs #

> ## gal\_cmd\_votemap <<sub><a href='cvarNotations.md'>i</a></sub>behavior> ##
> Indicates how the standard HL1 "**votemap**" command should function.
```
0 - disable
1 - behave normally
```
> Default value is "**0**".

> ## gal\_cmd\_listmaps <<sub><a href='cvarNotations.md'>i</a></sub>behavior> ##
> Indicates how the standard HL1 "**listmaps**" command should function.
```
0 - disable
1 - behave normally
2 - lists nominatable maps in a paginated format
```
> Default value is "**2**".

> ## gal\_nom\_mapfile <<sub><a href='cvarNotations.md'>c</a></sub>filename> ##
> Specifies the file to use which holds the names of the maps, listed one per line, that players can nominate.

> Use an asterisk to allow all maps in the server's maps folder to be nominatable instead of setting this value to the name of a file.

> When set to a filename without a path, it assumes the file is in the gamemod folder (i.e. **"cstrike/mapcycle.txt"**).  You can specify a relative path from your gamemod folder before the filename to use files located elsewhere (i.e. **"/addons/amxmodx/configs/mapcycle.txt"**).

> Default value is **"mapcycle.txt"**.

> ## gal\_listmaps\_paginate <<sub><a href='cvarNotations.md'>i</a></sub>mapCount> ##

> Specifies how many maps per "page" to show when using the "**listmaps**" console command.

> Paginating the map listings will prevent players from getting kicked when they are listing a large number of maps. When paginated, the listings will only display a portion of the total map list at a time.

> Setting it to "**0**" will not paginate the map listing.

> Default value is "**10**".


---

# Related Console Commands #

> ## votemap <<sub><a href='cvarNotations.md'>i</a></sub>mapID> ##
> The standard behavior of this HL1 command is to allow a client to vote for a particular map.

> When "**gal\_cmd\_votemap**" is set to "**0**" the client will be presented with a message indicating the command is disabled.

> When "**gal\_cmd\_votemap**" is set to "**1**" the command will function according to it's normal standard behavior.

> ## listmaps ##
> This default HL1 command lists the maps available on the server that the client can vote for - the server admin specifies which maps get listed by editing the mapcycle.txt file.

> When "**gal\_cmd\_listmaps**" is set to "**0**" the client will be presented with a message indicating the command is disabled.

> When "**gal\_cmd\_listmaps**" is set to "**1**" the command will function according to it's normal standard behavior.

> When "**gal\_cmd\_listmaps**" is set to "**2**" the list of maps will be taken from the file indicated by "**gal\_nom\_mapfile**" and will be displayed paginated according to the value of "**gal\_listmaps\_paginate**".