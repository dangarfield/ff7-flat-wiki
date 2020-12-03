---
title: Chocobo Races
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Technical](FF7/Technical.md) > Chocobo Races

### Symptoms

In Gold Saucer, whenever I go to Chocobo Races my game crashes to
Windows. I'm using Windows 2000 or XP.

### Causes

This is a very known problem caused by bad memory allocation. Game
refers to pointer that doesn't exist in memory and Windows XP doesn't
allow such operations.

### Solution

Eidos has no solution to this problem besides giving you Save so you can
play further in-game. This can be fixed using [Aali's OpenGL driver][].

[Back to Technical Problems page][]

  [Aali's OpenGL driver]: http://forums.qhimm.com/index.php?topic=8306.0
  [Back to Technical Problems page]: ../Technical.md "wikilink"