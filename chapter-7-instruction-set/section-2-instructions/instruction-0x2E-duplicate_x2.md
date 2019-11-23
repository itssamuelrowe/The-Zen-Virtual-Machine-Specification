# duplicate_x2

Duplicate the value on the top of the operand stack. The copy is inserted
below the first three values on top of the operand stack. This instruction
always copies a single byte. Remember that the operand stack is unaware
of value types.

## Byte Code
```
0x2E
```

## Format
```
duplicate_x2
```

## Operand Stack
**Before**  
```
    ..., value3, value2, value1
```
**After**  
```
    ..., value1, value3, value2, value1
```

## Operands
**value**  
    The value on top of the operand stack. It remains unchanged.  
**result**  
    A copy of the value is inserted below the fist three values on top
    of the operand stack.