---
title: E3 BGROL2
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Field](FF7/Field.md) > [Script](FF7/Field/Script.md) > [Opcodes](FF7/Field/Script/Opcodes.md) > E3 BGROL2

-   Opcode: **0xE3**
-   Short name: **BGROL2**
-   Long name: Background Roll (Reverse)

#### Memory layout

| 0xE3 | *B* | *A* |
|------|-----|-----|

#### Arguments

-   **const UByte** *B*: Bank to retrieve *A*, or zero if *A* is
    specified as a literal.
-   **const UByte** *A*: The ID of the background area to roll, as
    specified in the background's sprite.

#### Description

Similar to [BGROL][], except the roll runs backwards through layers,
rather than forwards. Rolling backwards past layer 0 for the area
specified results in no background being shown.

  [BGROL]: E2%20BGROL.md "wikilink"