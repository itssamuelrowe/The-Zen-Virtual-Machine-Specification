# cast_fti

Convert a `float` value to a `integer` value.

The following cases should be carefully observed:
 * A NaN value is always converted to `0`.
 * A finite value is rounded to an integer value using IEEE 754 round
   towards zero mode.
 * A negative value of very large magnitude or negative infinity is
   represented by the smallest integer value that occupies 32-bits.
 * A positive value of very large magnitude or positive infinity is
   represented by the largest integer value that occupies 32-bits.

The instruction narrows the `float` value. Therefore, loss of
information in regards to magnitude and precision may be observed.

## Byte Code
```
0x1B
```

## Format
```
cast_fi
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
    A 32-bit integer` value derived from converting the specified
    `float` value to integer` value. It is pushed onto
    the operand stack.