
---

# Description #
> Allowing an extension of the current map's time limit will add an "extend the map" option to map votes which, if the option wins, will increase the time limit by a predetermined amount, letting players stay on the current map longer.<br />


---

# Related CVARs #
> ## amx\_extendmap\_step <<sub><a href='cvarNotations.md'>f</a></sub>minutes> ##
> Specifies the number of minutes a map will be extended each time the "_Extend Map_" option wins the map vote.

> Default value is "**15**".

> This is the same CVAR that AMXX provides. It is duplicated in this plugin because Galileo is responsible for handling it.

> ## amx\_extendmap\_max <<sub><a href='cvarNotations.md'>f</a></sub>minutes> ##
> Specifies the maximum number of minutes a map can be played, if it has been extended. A value less than "**mp\_timelimit**" will not let the map be extended.

> Default value is "**90**".

> This is the same CVAR that AMXX provides. It is duplicated in this plugin because Galileo is responsible for handling it.

> ## mp\_timelimit <<sub><a href='cvarNotations.md'>f</a></sub>minutes> ##
> Specifies the number of minutes a map can be played, without it being extended.

> Setting it to "**0**" will let the map be played indefinitely.

> Default value is "**20**".

> This CVAR is not provided by this plugin. It is only being listed here as a reference since the value of it directly relates to this feature.