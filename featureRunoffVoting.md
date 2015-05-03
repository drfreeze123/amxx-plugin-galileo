
---

# Description #

> Runoff voting happens when none of the normal vote options receive over 50% of a given vote. The two options with the highest vote counts will be in the runoff vote.


---

# Related CVARs #

> ## gal\_runoff\_enabled _<_<sub><a href='cvarNotations.md'>i</a></sub>setting>_##_

> Indicates whether to allow runoff voting.
```
0 - disable runoff voting
1 - enable runoff voting
```
> Default value is "**1**".

> ## gal\_runoff\_duration _<_<sub><a href='cvarNotations.md'>i</a></sub>seconds>_##_

> Specifies the number of seconds the runoff vote should last.

> Default value is "**15**".

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