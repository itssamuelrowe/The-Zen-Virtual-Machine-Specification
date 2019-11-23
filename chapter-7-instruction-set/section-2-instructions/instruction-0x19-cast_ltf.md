# cast_ltf

Convert a 64-bit integer value to a 32-bit decimal value.

The conversion uses the IEEE 754 round to nearest mode.
The instruction widens the 64-bit integer value. However, loss of
information in regards to magnitude and precision may be observed.
This is because `float` has 24-bit significand bits.

## Byte Code
```
0x19
```

## Format
```
cast_ltf
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
    A 64-bit integer value. It is popped off the operand stack.  
**result**  
    A 32-bit `float` value derived from converting the specified
    32-bit integer value to 32-bit `float` value.
