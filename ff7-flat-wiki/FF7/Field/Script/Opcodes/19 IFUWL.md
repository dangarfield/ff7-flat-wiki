---
title: 19 IFUWL
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 19 IFUWL

-   Opcode: **0x19**
-   Short name: **IFUWL**
-   Long name: If (Unsigned Word, Long Jump)

#### Memory layout

| 0x19 | *B1 / B2* | *A* | *V* | *C* | *E* |
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
-   **const UShort** *E*: Amount to jump if the comparison does not
    hold.

#### Description

This is similar to the [IFUW][] opcode, but allows for a jump on
comparison failure of more than 0xFF bytes.

  [IFUW]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/18%20IFUW.md "wikilink"