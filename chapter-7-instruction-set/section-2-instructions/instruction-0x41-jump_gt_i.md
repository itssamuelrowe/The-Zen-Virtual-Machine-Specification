# jump_gt_i

Jump to the specified offset if `value1` is greater than `value2`, shown
as `value1 > value2`.

If the comparison succeeds, the `offset0` and `offset1` arguments are
used to evaluate a unsigned 16-bit offset, with the expression
`(offset0 << 8) | offset1`. The control is transferred to the instruction
at this offset. The offset should point to a valid byte within the byte
code range.

If the comparison fails, the control transfers to the instruction following
this instruction.

## Byte Code
```
0x41
```

## Format
```
jump_gt_i offset0 offset1
```

## Operand Stack
**Before**  
```
    ..., value1, value2
```
**After**  
```
    ...
```

## Operands
**value1**  
    A 32-bit integer value. It is popped off the operand stack.  
**value2**  
    A 32-bit integer value. It is popped off the operand stack.  
**result**  
    This instruction generates no result.