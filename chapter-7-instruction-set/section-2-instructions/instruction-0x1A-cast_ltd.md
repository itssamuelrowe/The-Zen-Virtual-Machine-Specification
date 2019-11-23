# cast_ltd

Convert a 64-bit integer value to a 64-bit decimal value.

The conversion uses the IEEE 754 round to nearest mode.
The instruction widens the 64-bit integer value. However, loss of
information in regards to magnitude and precision may be observed.
This is because `double` has 53-bit significand bits.

## Byte Code
```
0x1A
```

## Format
```
cast_ltd
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
    A 64-bit `double` value derived from converting the specified
    64-bit integer value to 64-bit `double` value.