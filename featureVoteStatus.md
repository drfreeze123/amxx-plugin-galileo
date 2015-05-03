# Description #

> By showing the status of the vote, you allow players to see how many votes the various choices received.

# Related CVARs #

> ## gal\_vote\_showstatus _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##
> Indicates when the vote progress should be shown to a player.
```
0 - never
1 - after player has voted
2 - after the vote ends
```
> Default value is "**1**"._

> ## gal\_vote\_showstatustype _<_<sub><a href='cvarNotations.md'>i</a></sub>style>_##
> Indicates how to show the progress of a vote.
```
1 - as vote count
2 - as percentage of all votes cast
```
> Default value is "**2**"._

> The value of this CVAR is irrelevant if **gal\_vote\_showstatus** is set to **0**.