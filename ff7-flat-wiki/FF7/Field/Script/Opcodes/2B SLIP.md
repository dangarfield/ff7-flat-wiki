---
title: 2B SLIP
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 2B SLIP

-   Opcode: **0x2B**
-   Short name: **SLIP**
-   Long name: Slipability

#### Memory layout

| 0x2B | *S* |
|------|-----|

#### Arguments

-   **const UByte** *S*: On/off switch (0/1, respectively).

#### Description

If SLIP is set to off, the player will be unable to let the playable
character run *against* and *along* the wall by pressing two buttons
together. For example, if there is a wall beyond the character running
left-to-right, and the character presses up and right together, the
character will normally run to the right along the wall. If SLIP is off,
the character will stop moving until the player presses right by itself;
the combination of up and right together is disallowed. This is
sometimes used in areas such as shops.

This should be used in combination with a [LINE][] to specify the line
along which the player may not 'slip'.

  [LINE]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/D0%20LINE.md "wikilink"