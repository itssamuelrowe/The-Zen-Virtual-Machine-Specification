# cast_itl

Convert a 32-bit integer value to a 64-bit integer value.

The instruction widens the 32-bit integer value. Therefore, loss of
information in regards to magnitude and precision is not observed.

In other words, the 32-bit integer is expanded to 64-bit integer, then
the sign is extended to a 64-bit result.

## Byte Code
```
0x13
```

## Format
```
cast_itl
```

## Operand Stack
**Before**  
```
    ..., value
```
**After**  
```
    ..., result
```

## Operands
**value**  
    A 32-bit integer value. It is popped off the operand stack.  
**result**  
    A 64-bit integer` value derived from converting the specified
    32-bit integer value to 64-bit integer value. The sign is extended to
    a 64-bit integer before it is pushed onto the operand stack.
