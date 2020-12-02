---
title: A2 DFANM
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > A2 DFANM

-   Opcode: **0xA2**
-   Short name: **DFANM**
-   Long name: Animate, Loop

#### Memory layout

| 0xA2 | *A* | *S* |
|------|-----|-----|

#### Arguments

-   **const UByte** *A*: Animation ID for this entity's field object.
-   **const UByte** *S*: Speed the animation is played at. Higher
    numbers indicate slower animations.

#### Description

Plays the animation given by *A* at the speed *S*. The animation loops
(plays, completes, then rewinds and plays again) until another animation
is played, either using any animation opcode, or an opcode indirectly
changes the animation being played, such as [MOVE][].

Makou Reactor Description: Play loop animation \#%1 of the field model
(speed=%2)

  [MOVE]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/A8%20MOVE.md "wikilink"