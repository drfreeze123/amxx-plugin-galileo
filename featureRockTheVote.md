
---

# Description #

> Rocking the vote is a way players can indicate their desire to start an early vote to change maps. Once enough players have rocked it, a vote will begin.


---

# Related CVARs #

> ## gal\_rtv\_commands _<_<sub><a href='cvarNotations.md'>i</a></sub>flags>_##
> Indicates which say commands can be used to rock the vote._

> The flags are additive. A value of "**0**" will disable this feature.
```
1 - standard "rockthevote" command
2 - shorthand "rtv" command
4 - dynamic "rockthe<anything>vote" command (allows a player to type any one
    word that starts with "rockthe" and ends with "vote". Some examples might 
    be "rockthedamnvote", "rockthesillylittlevote", or "rockthefreakingvote".
    The total length of the word can not be longer than 20 characters. 
```
> The default is "**3**" _(1 + 2 = 3)_.

> ## gal\_rtv\_wait _<_<sub><a href='cvarNotations.md'>i</a></sub>minutes>_##
> Specifies the number of minutes after a map starts that players have to wait before they can rock the vote._

> When a single player is on the server, that player can rock the vote at any time, regardless of this setting.

> The default is "**10**".

> ## gal\_rtv\_ratio _<_<sub><a href='cvarNotations.md'>f</a></sub>ratio>_##
> Specifies the ratio of players that need to rock the vote before a vote will be forced to occur. When a single player is on the server, that player can rock the vote and start an immediate vote._

> The default is "**0.60**".

> ## gal\_rtv\_reminder _<_<sub><a href='cvarNotations.md'>i</a></sub>minutes>_##
> Specifies how often, in minutes, to remind everyone how many more rocks are still needed, after the last rock has been made._

> A value of "**0**" indicates no periodic reminders will be given.

> The default is "**2**".

> Regardless of the value of this setting, the player will always get immediate feedback, when rocking the vote, letting them know how many more rocks are needed.

> ## gal\_rtv\_disableflags _<_<sub><a href='cvarNotations.md'>c</a></sub>[accessFlags](http://wiki.alliedmods.net/Adding_Admins_(AMX_Mod_X)#Access_Levels)>_##
> Indicates if the "rock the vote" feature is disabled while players with the specified  [access flags](http://wiki.alliedmods.net/Adding_Admins_(AMX_Mod_X)#Access_Levels) are in game._

> You can specify multiple flags.

> An empty value means the ability to rock the vote is not dependent on whether admins are present.

> The default is **""**.


---

# Related Say Commands #

> ## rockthevote | rtv | rockthe_`<`anything`>`_vote ##
> Registers the player's desire for an early map vote. The player will be informed how many more players need to rock the vote before a vote will be forced.

> The _anything_ argument can be any word up to 20 characters in length.

> Requires an appropriate value set for "**gal\_rtv\_commands**".