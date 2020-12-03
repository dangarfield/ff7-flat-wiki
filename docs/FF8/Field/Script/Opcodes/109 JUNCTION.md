---
title: 109 JUNCTION
---

[Home](Main%20Page.md) > [FF8](FF8.md) > [Field](FF8/Field.md) > [Script](FF8/Field/Script.md) > [Opcodes](FF8/Field/Script/Opcodes.md) > 109 JUNCTION

-   Opcode: **0x0109**
-   Short name: **JUNCTION**
-   Long name: Set "dream world" status

#### Argument

none

#### Stack

  
*Junction mode*

**JUNCTION**

#### Description

  
When set to 0, ends all "dream world" related stuff (GF junction
carryover, Squall-&gt;Laguna, party lock, etc).

When set to 1, only Squall's junctions gets carried over.

When set to 3, the whole party gets carried over.