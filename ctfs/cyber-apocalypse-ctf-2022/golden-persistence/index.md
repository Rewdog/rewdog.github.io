---
layout: default
title: Golden Persistence | Cyber Apocalypse CTF 2022 from HackTheBox
---
# [Cyber Apocalypse CTF 2022 from HackTheBox](../) - Golden Persistence

* **Category:** Forensics
* **Points:** 300 points

## Challenge

> Emergency! A space station near Urkir was compromised. Although Urkir is considered to be the very embodiment of the neutral state, it is rich of fuel substances, something that Dreager is very much interested in. Thus, there are now fears that the intergalactic war will also affect this neutral planet. If Draeger and his mercenaries manage to maintain unauthorised access in Urkir's space station and escalate their privileges, they will soon be able to activate the station's defence mechanisms that are able to prevent any spaceship from entering Urkir's airspace. For now, the infected machine is isolated until the case is closed. Help Miyuki find their persistence mechanisms so they cannot gain access again.

## TL;DR
NTUSER.dat has a powershell command running a base64 encoded script that allows the decryption of strings, and specifies some registry locations to find target strings. Use `reglookup` to get the values of those strings, and find the flag in the final command.

## Solution

Coming Soon

```
HTB{g0ld3n_F4ng_1s_n0t_st34lthy_3n0ugh}
```