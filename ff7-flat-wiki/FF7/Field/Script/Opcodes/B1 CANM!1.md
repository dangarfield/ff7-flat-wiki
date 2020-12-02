---
title: B1 CANM!1
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > B1 CANM!1

-   Opcode: **0xB1**
-   Short name: **CANM!1**
-   Long name: Particial Animation.

#### Memory layout

| 0xAF | *A* | *F* | *L* | *S* |
|------|-----|-----|-----|-----|

#### Arguments

-   **const UByte** *A*: Animation ID for this entity's field object.
-   **const UByte** *F*: First frame of animation.
-   **const UByte** *L*: Last frame of animation.
-   **const UByte** *S*: Relative speed of animation. Real model
    animation speed divide by this to calculate real play speed.

#### Description

Exactly the same as [ANIM!1][], but allow set first and last frame of
given animation.

Makou Reactor Description: Play partially the animation \#%1 of the
field model (first frame=%2, last frame=%3, speed=%4)

  [ANIM!1]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/AF%20ANIM!1.md "wikilink"