---
title: A6 XYI
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > A6 XYI

-   Opcode: **0xA6**
-   Short name: **XYI**
-   Long name: Place Object (No Z)

#### Memory layout

| 0xA6 | *B1 / B2* | *B3 / 0* | *X* | *Y* | *I* |
|------|-----------|----------|-----|-----|-----|

#### Arguments

-   **const Bit\[4\]** *B1*: Bank to retrieve *X*, or zero if *X* is
    specified as a literal value.
-   **const Bit\[4\]** *B2*: Bank to retrieve *Y*, or zero if *Y* is
    specified as a literal value.
-   **const Bit\[4\]** *B3*: Bank to retrieve *I*, or zero if *I* is
    specified as a literal value.
-   **const Bit\[4\]** *0*: Zero.
-   **const Short** *X*: X-coordinate of the field object, or address of
    X-coordinate if *B1* is non-zero.
-   **const Short** *Y*: Y-coordinate of the field object, or address of
    Y-coordinate if *B2* is non-zero.
-   **const UShort** *Z*: Triangle ID, or address of ID if *B3* is
    non-zero.

#### Description

Similar to [XYZI][], but does not specify a Z-coordinate. This lack of
Z-coordinate may be a problem when placing the object on a mesh that has
multiple Z-levels on the same X- and Y-coordinates.

  [XYZI]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/A5%20XYZI.md "wikilink"