---
title: 18 IFUW
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 18 IFUW

-   Opcode: **0x18**
-   Short name: **IFUW**
-   Long name: If (Unsigned Word)

#### Memory layout

| 0x18 | *B1 / B2* | *A* | *V* | *C* | *E* |
|------|-----------|-----|-----|-----|-----|

#### Arguments

-   **const Bit\[4\]** *B1*: First memory bank to access.
-   **const Bit\[4\]** *B2*: Second memory bank to access.
-   **const UShort** *A*: Address, from the first bank, of the value to
    retrieve.
-   **const UShort** *V*: Unsigned value to compare the retrieved value
    to, or address from the second bank of the value to retrieve, if
    *B2* is non-zero.
-   **const UByte** *C*: Type of comparison to perform.
-   **const UByte** *E*: Amount to jump if the comparison does not hold.

#### Description

This is similar to the [IFUB][] opcode, but it allows the value to be
larger than 0xFF.

  [IFUB]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/14%20IFUB.md "wikilink"