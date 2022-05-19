---
layout: default
title: Entrypoint | Cyber Apocalypse CTF 2022 from HackTheBox
---
# [Cyber Apocalypse CTF 2022 from HackTheBox](../) - Space Pirate: Entrypoint

* **Category:** Pwn
* **Points:** 300 points

## Challenge

> D12 is one of Golden Fang's missile launcher spaceships. Our mission as space pirates is to highjack D12, get inside the control panel room, and access the missile launcher system. To achieve our goal, we split the mission into three parts. In this part, all we need to do is bypass the scanning system and open the gates so that we proceed further.


## TL;DR
Put pretty much anything into password other than `0nlyTh30r1g1n4lCr3wM3mb3r5C4nP455` and it give you the flag.

## Solution

Not sure if this was intentional, but just putting in `hello` in the password gave me the flag. Looking at the code in ghidra, it seems to do a comparison on `0nlyTh30r1g1n4lCr3wM3mb3r5C4nP455`, and sending that string doesn't give you the flag. 

```
1. Scan card 💳
2. Insert password ↪️
> 2
[*] Insert password: hello

[+] Door opened, you can proceed with the passphrase: HTB{th3_g4t35_4r3_0p3n!} 

```

```
HTB{th3_g4t35_4r3_0p3n!}
```
