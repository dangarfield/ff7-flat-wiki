---
title: 97_DEC
---

[Home](../../../../Main_Page.md) > [FF7](../../../../FF7.md) > [Field](../../../Field.md) > [Script](../../Script.md) > [Opcodes](../Opcodes.md) > 97 DEC

-   Opcode: **0x97**
-   Short name: **DEC**
-   Long name: Decrement (8-bit)

#### Memory layout

| 0x97 | *B* | *A* |
|------|-----|-----|

#### Arguments

-   **const UByte** *B*: Destination bank.
-   **const UByte** *A*: Address.

#### Description

Decrements the 8-bit value found at bank **B**, address **A**. If the value is 0x00, it will roll over to 0xFF. If you specify a 16-bit bank, only the lower byte will be decremented, and if the lower byte is 0x00, the higher byte will be unaffected whilst the lower byte will return to 0xFF.