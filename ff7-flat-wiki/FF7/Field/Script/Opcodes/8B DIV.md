---
title: 8B DIV
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 8B DIV

-   Opcode: **0x8B**
-   Short name: **DIV**
-   Long name: Division (8-bit)

#### Memory layout

| 0x8B | *D/S* | *Dest* | *Den* |
|------|-------|--------|-------|

#### Arguments

-   **const Bit\[4\]** *D*: Destination bank
-   **const Bit\[4\]** *S*: Source bank
-   **const UByte** *Dest*: Contains the nominator of the division and
-   **const UByte** *Den*: The denominator of the division.

#### Description

Divides â€œDestâ€ by â€œDenâ€ and stores the result back into
â€œDestâ€. The result of the division is rounded towards zero to the
nearest integer. If the Source Bank is 0 then the â€œDenâ€ is the
denominator. If the Source Bank is an 8 bit bank, then the â€œDenâ€ is
the address in that bank where the denominator is.