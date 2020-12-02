---
title: 55 WROW
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 55 WROW

-   Opcode: **0x55**
-   Short name: **WROW**
-   Long name: Window Rows

#### Memory layout

| 0x55 | *N* | *R* |
|------|-----|-----|

#### Arguments

-   **const UByte** *N*: The ID of the [WINDOW][] whose height will be
    set.
-   **const UByte** *R*: Number of rows of text that should fit in this
    window.

#### Description

Sets the height of the window with ID *N*, by adjusting it to fit a
specified number of rows of text, as given by *R*. If the dialog does
not fit after adjusting the height of the window, the player will be
able to scroll the dialog in the window by pressing \[OK\] to see the
proceeding lines of text. When all text has scrolled, the window will
close as normal.

  [WINDOW]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/50%20WINDOW.md "wikilink"