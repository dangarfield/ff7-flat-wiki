---
title: F1 SOUND
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Field](FF7/Field.md) > [Script](FF7/Field/Script.md) > [Opcodes](FF7/Field/Script/Opcodes.md) > F1 SOUND

-   Opcode: **0xF1**
-   Short name: **SOUND**
-   Long name: Play Sound

#### Memory layout

| 0xF1 | *B1 / B2* | *I* | *D* |
|------|-----------|-----|-----|

#### Arguments

-   **const Bit\[4\]** *B1*: Source bank 1, or zero if *I* is set as a
    constant value.
-   **const Bit\[4\]** *B2*: Source bank 2, or zero if *D* is set as a
    constant value.
-   **const UShort** *I*: [Sound ID][] to play, or lower byte indicating
    address and higher byte zero, if *B1* is non-zero.
-   **const UByte** *D*: Directional sound, or address to find direction
    value, if *B2* is non-zero.

#### Description

Plays the sound file indicated by *I*, or if *B1* is non-zero, plays the
sound with ID found at bank *B1* and address *I*. The direction of the
sound can also be specified, with 0 indicating the left speaker, 40
indicating center, and 7F indicating the right speaker.

  [Sound ID]: ../../Sound%20ID%20Table.md "wikilink"