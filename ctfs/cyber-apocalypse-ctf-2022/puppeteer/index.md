---
layout: default
title: Puppeteer | Cyber Apocalypse CTF 2022 from HackTheBox
---
# [Cyber Apocalypse CTF 2022 from HackTheBox](../) - Puppeteer

* **Category:** Forensics
* **Points:** 300 points

## Challenge

> Planet Longhir is known for it's top-tier researchers. Due to their dedication in science and engineering, their military equipment is the most advanced one in the galaxy. In fact, the prototype DES-3000, a self-propelled precision-strike missile that is capable of reaching targets even in Ratnik galaxy, is being used to disable Galactic Federation's communication satellites. The mystery that Miyuki is trying to solve is, how the satellite's location was leaked since it is a top-sercret that only Galactic Federation's council is aware of. Help her analyse the Council's HQ event logs and solve this mystery.

## TL;DR
Use `evtx_dump` to obtain a powershell script from `Microsoft-Windows-WMI-Activity%4Operational.evtx`. Strip out a bunch of the exploitation commands, and run the script to get the flag.

## Solution

Coming Soon

```powershell
[byte[]] $stage1 = 0x99, 0x85, 0x93, 0xaa, 0xb3, 0xe2, 0xa6, 0xb9, 0xe5, 0xa3, 0xe2, 0x8e, 0xe1, 0xb7, 0x8e, 0xa5, 0xb9, 0xe2, 0x8e, 0xb3;
[byte[]] $stage2 = 0xac, 0xff, 0xff, 0xff, 0xe2, 0xb2, 0xe0, 0xa5, 0xa2, 0xa4, 0xbb, 0x8e, 0xb7, 0xe1, 0x8e, 0xe4, 0xa5, 0xe1, 0xe1;
[array]::Reverse($stage2);

$stage3 = $stage1 + $stage2;

#Unpack Special Orders!
for($i=0;$i -lt $stage3.count;$i++){
    $stage3[$i] = $stage3[$i] -bxor 0xd1;
}
[System.Text.Encoding]::ASCII.GetString($stage3)
```

```
HTB{b3wh4r3_0f_th3_b00t5_0f_just1c3...}
```
