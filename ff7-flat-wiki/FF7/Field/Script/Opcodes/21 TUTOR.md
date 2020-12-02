---
title: 21 TUTOR
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 21 TUTOR

-   Opcode: **0x21**
-   Short name: **TUTOR**
-   Long name: Play Tutorial

#### Memory layout

| 0x21 | *T* |
|------|-----|

#### Arguments

-   **const UByte** *T*: Tutorial ID.

#### Description

Opens the main menu and plays the tutorial specified. The tutorial with
the given ID must exist in the field file (PlayStation) or inside the
flevel.lgp archive (PC), or the menu will not be closable.

On the PlayStation version, the tutorials reside after the dialog and
AKAO blocks of Section 1. On the PC version, the same tutorials can be
found in this location, but are not used and redundant since the dialogs
are PlayStation-specific, such as "You'll need a Memory Card to save
your games". Instead, the PC-specific tutorials are used, which are
located in the flevel.lgp archive and end with the extension **.tut**.