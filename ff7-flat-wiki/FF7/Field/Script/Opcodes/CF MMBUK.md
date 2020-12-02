---
title: CF MMBUK
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > CF MMBUK

-   Opcode: **0xCF**
-   Short name: **MMBUK**
-   Long name: Party Select: Character Unlock

#### Memory layout

| 0xCF | *C* |
|------|-----|

#### Arguments

-   **const UByte** *C*: Character ID to unlock.

#### Description

Unocks the character given by the argument in the Party Select screen.
The player will be able to move this character into or out of the party.
The character IDs can be found in [MMBud][].

This setting has global scope, that is, the character will still be
switchable when transitioning to a new field or to the world map and
using the PHS.

  [MMBud]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/CD%20MMBud.md "wikilink"