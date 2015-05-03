<table align='right' valign='top'><tr><td>
<hr />
<h1>Related Features</h1>
<ul><li><a href='featureNextmapVoting.md'>Next Map Voting</a>
<hr />
</td></tr></table></li></ul>

# Introduction #

This feature allows you to prioritize different groups of maps to use in filling a vote. It allows you to say, "pick up to X maps from this group first, then pick up to Y maps from this other group". You can have a maximum of 8 groups.

# Details #

Here is an example of 3 counts listed:
```
3
3
2
```

The counts should not total more than the number of maps you allow in the vote. In the case of this example, the counts add up to 8 (3+3+2=8), which happens to be the maximum number of maps that can be allowed in a vote.

Since I've listed three different counts, I'll need 3 different files to keep my map listings in.

The files must be named and located as such:
```
./amxmodx/configs/galileo/1.ini
./amxmodx/configs/galileo/2.ini
./amxmodx/configs/galileo/3.ini
```
Each of those files, **1.ini**, **2.ini**, and **3.ini**, should contain a listing of maps [in the style of](fileMapcycle_txt#In_the_Style_of....md) **mapcycle.txt**.

Galileo will first load any nominated maps into the vote. It will then grab up to 3 maps from **1.ini**, up to 3 from **2.ini**, and up to 2 from **3.ini**.

# Map Load Order #

Maps will be loaded according to the order below until the maximum number of maps has been loaded as specified by **gal\_vote\_mapchoices**.
  1. nominated maps
  1. maps from vote fill groups
  1. maps specified by **gal\_vote\_mapfile**