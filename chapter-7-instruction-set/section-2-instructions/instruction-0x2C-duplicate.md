# duplicate

Duplicate the value on the top of the operand stack. The copy is inserted
at the top of the operand stack. This instruction always copies a single
byte. Remember that the operand stack is unaware of value types.

## Byte Code
```
0x2C
```

## Format
```
duplicate
```

## Operand Stack
**Before**  
```
    ..., value
```
**After**  
```
    ..., value, value
```

## Operands
**value**  
    The value on top of the operand stack. It remains unchanged.
    In fact, a copy of this value is pushed onto the operand stack.  
**result**  
    A duplicate of the value on top of the operand stack.