---
title: 00 RET
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [Field](/ff7-flat-wiki/FF7/Field.md) > [Script](/ff7-flat-wiki/FF7/Field/Script.md) > [Opcodes](/ff7-flat-wiki/FF7/Field/Script/Opcodes.md) > 00 RET

-   Opcode: **0x00**
-   Short name: **RET**
-   Long name: Return from request / Halt

#### Memory layout

| 0x00 |
|------|

#### Arguments

None.

#### Description

When an [entity][]'s script is being executed as part of a request
(function call), the return opcode will cause current execution to halt
and return to whatever the entity was previously executing (at some
lower [priority][]). If the execution was requested via a synchronous
call ([REQEW][] or [PRQEW][]), the completion of execution is also
signalled to the calling entity which can resume execution.

If *return* is used when executing at base priority, execution will
simply halt. This is what happens in the [entry scripts][].

  [entity]: /ff7-flat-wiki/FF7/Field/Script/Entity.md "wikilink"
  [priority]: /ff7-flat-wiki/FF7/Field/Script/Priorities.md "wikilink"
  [REQEW]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/03%20REQEW.md "wikilink"
  [PRQEW]: /ff7-flat-wiki/FF7/Field/Script/Opcodes/06%20PRQEW.md "wikilink"
  [entry scripts]: /ff7-flat-wiki/FF7/Field/Scripts/Entry%20script.md "wikilink"