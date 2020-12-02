---
title: 2C BGPDH
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 2C BGPDH

-   Opcode: **0x2C**
-   Short name: **BGPDH**
-   Long name: Background Depth

#### Memory layout

| 0x2C | *B / 0* | *L* | *D* |
|------|---------|-----|-----|

#### Arguments

-   **const Bit\[4\]** *B*: Bank to retrieve value for *D*, or zero if
    *D* is specified as a literal.
-   **const Bit\[4\]** *0*: Four zero bits.
-   **const UByte** *L*: ID number of the layer to manipulate.
-   **const Short** *D*: Z-depth of the specified layer, or the address
    to find *D* if *B* is non-zero.

#### Description

Sets the Z-depth for the extra background layer specified by *L*. This
opcode will only set the depth of those extra layers above the standard
background and foreground layers (0/1, respectively), and so should be
an argument of 2 or greater.