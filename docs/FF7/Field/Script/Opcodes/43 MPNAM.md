---
title: 43 MPNAM
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Field](FF7/Field.md) > [Script](FF7/Field/Script.md) > [Opcodes](FF7/Field/Script/Opcodes.md) > 43 MPNAM

-   Opcode: **0x43**
-   Short name: **MPNAM**
-   Long name: Map Name

#### Memory layout

| 0x43 | *D* |
|------|-----|

#### Arguments

-   **const UByte** *D*: Dialog ID.

#### Description

Sets the name of this map to the dialog ID given by *D*. The map name is
found in the box in the bottom-right of the main menu, below the time
and gil box.