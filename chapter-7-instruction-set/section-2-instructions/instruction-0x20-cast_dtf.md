# cast_dtf

Convert a `double` value to a `float` value.

The specified `double` value is converted to a `float`
value using IEEE 754 round to nearest mode. In other words, the
instruction narrows the `double` value. Therefore, loss of
information in regards to magnitude and precision may be observed.

The following cases should be carefully observed:
 * Values too small to represent as a `float` value is represented
   as zero.
 * Values too big to represents as a `float` value is represented
   as infinity.
In both cases, the sign of the value is always retained.

## Byte Code
```
0x20
```

## Format
```
cast_df
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
    A 64-bit `double` value. It is popped off the operand stack.  
**result**  
    A 32-bit float value derived from converting the specified
    `double` value to `float` value. It is pushed onto
    the operand stack.