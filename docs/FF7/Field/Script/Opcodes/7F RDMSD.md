---
title: 7F RDMSD
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Field](FF7/Field.md) > [Script](FF7/Field/Script.md) > [Opcodes](FF7/Field/Script/Opcodes.md) > 7F RDMSD

-   Opcode: **0x7F**
-   Short name: **RDMSD**
-   Long name: Seed Random Generator

#### Memory layout

| 0x7F | *B* | *S* |
|------|-----|-----|

#### Arguments

-   **const UByte** *B*: Bank in which the seed value is stored, or zero
    if *S* is specified as a literal value.
-   **const UByte** *S*: Seed for the random generator, or address for
    the seed if *B* is non-zero.

#### Description

Seeds the random number generator used by [RANDOM][]. The lower four
bits of the arguments are used as the seed value by altering the offset
used to take a value from the table of pseudo-random numbers.

  [RANDOM]: 99%20RANDOM.md "wikilink"