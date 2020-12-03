---
title: 40 MESSAGE
---

[Home](Main%20Page.md) > [FF7](FF7.md) > [Field](FF7/Field.md) > [Script](FF7/Field/Script.md) > [Opcodes](FF7/Field/Script/Opcodes.md) > 40 MESSAGE

-   Opcode: **0x40**
-   Short name: **MESSAGE**
-   Long name: Message display

#### Memory layout

| 0x40 | *N* | *D* |
|------|-----|-----|

#### Arguments

-   **const UByte** *N*: The ID of the window to use.
-   **const UByte** *D*: The zero-based index of the [dialog][] that
    will be displayed.

#### Description

Displays a dialog in the [WINDOW][] that has previously been initialised
to display this dialog.

  [dialog]: ../../Script.md "wikilink"
  [WINDOW]: 50%20WINDOW.md "wikilink"