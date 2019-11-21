# jump_eqn_a

Jump to the specified offset if `value` is equal to `null`, shown as
`value1 == null`.

If the comparison succeeds, the `offset0` and `offset1` arguments are
used to evaluate a unsigned 16-bit offset, with the expression
`(offset0 << 8) | offset1`. The control is transferred to the instruction
at this offset. The offset should point to a valid byte within the byte
code range.

If the comparison fails, the control transfers to the instruction following
this instruction.

## Byte Code
```
0x46
```

## Format
```
jump_eqn_a offset0 offset1
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
    A reference value. The size is contingent on the machine, which is
    transparent to the binary entity format. The value is popped off the
    operand stack.  
**result**  
    This instruction generates no result.