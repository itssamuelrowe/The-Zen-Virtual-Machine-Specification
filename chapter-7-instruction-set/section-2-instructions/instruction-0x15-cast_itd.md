# cast_itd

Convert a 32-bit integer value to a 64-bit decimal value.

The conversion uses the IEEE 754 round to nearest mode.
The instruction widens the 32-bit integer value. Therefore, loss of
information in regards to magnitude and precision is not observed.
This is because `double` has 53-bit significand bits.

## Byte Code
```
0x15
```

## Format
```
cast_itd
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
    A 64-bit `double` value derived from converting the specified
    32-bit integer value to 64-bit `double` value.