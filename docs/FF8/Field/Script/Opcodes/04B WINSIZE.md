---
title: 04B WINSIZE
---

[Home](Main%20Page.md) > [FF8](FF8.md) > [Field](FF8/Field.md) > [Script](FF8/Field/Script.md) > [Opcodes](FF8/Field/Script/Opcodes.md) > 04B WINSIZE

-   Opcode: **0x04B**
-   Short name: **WINSIZE**
-   Long name: Set Window Size

#### Argument

none

#### Stack

  
*Message Channel*

*X*

*Y*

*Width*

*Height*

**WINSIZE**

#### Description

Sets the window location and size for the given message channel. Only
useful before calling MES, which has no built-in size parameters.
WINSIZE is only used in the first hallway of the game, where Quistis is
imitating Squall (and also in some debug areas). Probably, Square's
eventers used this a few times, hated how tedious it was, and asked for
the AMES family of opcodes to be added, but didn't change the ones they
already did.