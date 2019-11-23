# jump_eq0_i

Jump to the specified offset if `value` is equal to `0`, shown as
`value == 0`.

If the comparison succeeds, the `offset0` and `offset1` arguments are
used to evaluate an unsigned 16-bit offset, with the expression
`(offset0 << 8) | offset1`. The control is transferred to the instruction
at this offset. The offset should point to a valid byte within the byte
code range.

If the comparison fails, the control transfers to the instruction following
this instruction.

## Byte Code
```
0x38
```

## Format
```
jump_eq0_i offset0 offset1
```

## Operand Stack
**Before**  
```
    ..., value
```
**After**  
```
    ...
```

## Operands
**value**  
    A 32-bit integer value. It is popped off the operand stack.  
**result**  
    This instruction generates no result.