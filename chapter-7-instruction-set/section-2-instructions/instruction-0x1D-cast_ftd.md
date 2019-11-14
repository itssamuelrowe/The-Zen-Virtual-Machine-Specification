# cast_ftd

Convert a `float` value to a `double` value.

The specified `float` value is converted to a `double`
value using IEEE 754 round to nearest mode. In other words, the
instruction widens the `float` value. Therefore, no loss of
information in regards to magnitude and precision may be observed.

## Byte Code
```
0x1D
```

## Format
```
cast_fd
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
    A 32-bit `float` value. It is popped off the operand stack.  
**result**  
    A 64-bit `double` value derived from converting the specified
    `float` value to `double` value. It is pushed onto
    the operand stack.""
