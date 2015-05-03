
---

# Description #

> Banning recently played maps means that the last several maps that have been played can not be nominated or otherwise placed in the map vote. This ensures that a map can not be played over and over again at the expense of playing a variety of other maps.


---

# Related CVARs #

> ## gal\_banrecent <<sub><a href='cvarNotations.md'>i</a></sub>mapCount> ##
> Specifies how many of the most recent maps are disallowed from a map vote.

> A value of "**0**" will disable this feature.

> Default value is "**3**".

> There is a cap defined by the "MAX\_RECENT\_MAP\_CNT" constant in the SMA. It is set to "**16**" by default. It's not recommended but it can be safely changed if needed. The value of this CVAR needs to be less than or equal to the value of "MAX\_RECENT\_MAP\_CNT".

> ## gal\_banrecentstyle <<sub><a href='cvarNotations.md'>i</a></sub>style> ##
> Indicates the style in which the recent maps are displayed when a player uses the "**recentmaps**" say command.
```
1 - all maps on one line
2 - each map on a separate line
```
> Default value is "**1**".


---

# Related Say Commands #

> ## recentmaps ##
> Displays a listing of the most recently played maps to all players.

> Requires "**gal\_banrecent**" to be set to a value higher than "**0**" or the command will not be available.