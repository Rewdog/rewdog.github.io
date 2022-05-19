---
layout: default
title: Rewdog.com
---
# [Cyber Apocalypse CTF 2022 from HackTheBox](../) - Mutation Lab

* **Category:** Web
* **Points:** 300 points

## Challenge

> One of the renowned scientists in the research of cell mutation, Dr. Rick, was a close ally of Draeger. The by-products of his research, the mutant army wrecked a lot of havoc during the energy-crisis war. To exterminate the leftover mutants that now roam over the abandoned areas on the planet Vinyr, we need to acquire the cell structures produced in Dr. Rick's mutation lab. Ulysses managed to find a remote portal with minimal access to Dr. Rick's virtual lab. Can you help him uncover the experimentations of the wicked scientist?

## TL;DR
Use [CVE-2021-23631 poc](https://gist.github.com/legndery/a248350bb25b8502a03c2f407cedeb14) to get LFI in order to read the app's cookie signing secret key at `file://./app/.env` . Then use [cookie-monster](https://www.npmjs.com/package/@digital-interruption/cookie-monster/v/1.0.2) to sign a new cookie for the user `admin`. Use that cookie to enable a new feature on the dashboard, which reveals the flag in an image.

## Solution

Coming Soon

```
HTB{fr4m3d_th3_s3cr37s_f0rg3d_th3_entrY}
```