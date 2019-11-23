# duplicate_x1

Duplicate the value on the top of the operand stack. The copy is inserted
below the first two values on top of the operand stack. This instruction
always copies a single byte. Remember that the operand stack is unaware
of value types.

## Byte Code
```
0x2D
```

## Format
```
duplicate_x1
```

## Operand Stack
**Before**  
```
    ..., value2, value1
```
**After**  
```
    ..., value1, value2, value1
```

## Operands
**value**  
    The value on top of the operand stack. It remains unchanged.  
**result**  
    A copy of the value is inserted below the fist two values on top
    of the operand stack.