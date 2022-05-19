---
layout: default
title: Rewdog.com
---
# [Cyber Apocalypse CTF 2022 from HackTheBox](../) - Compressor

* **Category:** Misc
* **Points:** 325 points

## Challenge

> Ramona's obsession with modifications and the addition of artifacts to her body has slowed her down and made her fail and almost get killed in many missions. For this reason, she decided to hack a tiny robot under Golden Fang's ownership called "Compressor", which can reduce and increase the volume of any object to minimize/maximize it according to the needs of the mission. With this item, she will be able to carry any spare part she needs without adding extra weight to her back, making her fast. Can you help her take it and hack it?


## TL;DR
Send `../../*flag*` into Option `3`, which prints the contents of any files with flag in the name.

## Solution

The challenge is a tcp service that gives you a first menu which doesn't seem to have any true value, and a second menu which wraps system commands. 

```
Actions:
1. Create artifact
2. List directory    (pwd; ls -la)
3. Read artifact     (cat ./<name>)
4. Compress artifact (zip <name>.zip <name> <options>)
5. Change directory  (cd <dirname>)
6. Clean directory   (rm -rf ./*)
7. Exit

[*] Choose action: 3

```

 `3. Read artifact     (cat ./<name>) ` didn't seem to have much validation on the input, so sending `../../*` prints all the contents of the directory in which the service is running, including the source code and the flag file. This can be simplified to specify any file with flag in the name.

```
Insert name you want to read: ../../*flag*
HTB{GTFO_4nd_m4k3_th3_b35t_4rt1f4ct5}
```
