---
title: 39 GOLDu
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 39 GOLDu

-   Opcode: **0x39**
-   Short name: **GOLDu**
-   Long name: Gil Up

#### Memory layout

| 0x39 | *0* | *A* |
|------|-----|-----|

| 0x39 | *B / 0* | *A* | *0* |
|------|---------|-----|-----|

#### Arguments

Increase by a constant amount:

-   **const UByte** *0*: Zero.
-   **const ULong** *A*: Amount to increase.

Increase by an amount found in memory:

-   **const Bit\[4\]** *B*: Source bank.
-   **const UByte** *A*: Source address.
-   **const UByte\[3\]** *0*: Three zero bytes.

#### Description

Increases the amount of gil by a constant amount, or by an amount found
in the source bank *B* and address *A*.

The total gil is capped above by 0xFFFFFFFF; attempts to increment
further will fail.