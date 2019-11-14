# duplicate2

Duplicate the first two values on the top of the operand stack. The copies
are inserted at the top of the operand stack. This instruction always copies
two bytes. Remember that the operand stack is unaware of value types.

## Byte Code
```
0x2F
```

## Format
```
duplicate2
```

## Operand Stack
**Before**  
```
    ..., value2, value1
```
**After**  
```
    ..., value2, value1, value2, value1
```

## Operands
**value1**  
    The value on top of the operand stack. It remains unchanged.  
**value2**  
    The value below the value on top of the operand stack. It remains
    unchanged.  
**result**  
    A duplicate of the first two values on top of the operand stack.