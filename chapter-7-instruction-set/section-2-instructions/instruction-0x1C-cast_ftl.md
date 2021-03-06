# cast_ftl

Convert a `float` value to a `double` value.

The following cases should be carefully observed:
 * A NaN value is always converted to `0`.
 * A finite value is rounded to an integer value using IEEE 754 round
   towards zero mode.
 * A negative value of very large magnitude or negative infinity is
   represented by the smallest signed integer value that occupies
   64-bits.
 * A positive value of very large magnitude or positive infinity is
   represented by the largest signed integer value that occupies
   64-bits.

The instruction narrows the `double` value. Therefore, loss of
information in regards to magnitude and precision may be observed.

## Byte Code
```
0x1C
```

## Format
```
cast_fl
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
    A 64-bit integer value derived from converting the specified
    `float` value to a long` value. It is pushed onto
    the operand stack.
