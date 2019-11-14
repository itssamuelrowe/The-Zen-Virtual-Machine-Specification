# divide_f

Divide two `float` values.

The following rules, in accordance with IEEE 754, should be observed
when dividing two `float` values.
 * If either the first or the second operand is NaN, the result is
   always NaN.
 * The result is positive if both the operands have the same sign.
 * The result is negative if both the operands have different signs.
 * The result is NaN if both the operands are infinities, regardless
   of their signs.
 * The result is positive infinity if an infinity is divided by a
   finite value with the same sign as the infinity.
 * The result is negative infinity if an infinity is divided by a
   finite value with the sign opposite to the sign of the infinity.
 * The result is positive zero if a finite value is divied by an
   infinity with the same sign as the finite value.
 * The result is negative zero if a finite value is divied by an
   infinity with the sign opposite to the finite values sign.
 * The result is NaN if a zero is divided by a zero, regardless of
   the signs.
 * The result is positive zero if a zero is divided by a finite
   value with the same sign as the zero.
 * The result is negative zero if a zero is divided by a finite
   value with the sign opposite to the sign of zero.
 * The result is positive infinity if a finite value (other than
   zero) is divided by zero with the same sign as the finite value.
 * The result is negative infinity if a finite value (other than
   zero) is divided by zero with the sign opposite to the sign of
   the finite value.
 * In all other cases, where neither operand is an infinity, a
   zero, or NaN, the quotient is computed and rounded to the nearest
   representable value using IEEE 754 round to nearest mode. If
   the magnitude is too large to represent as a `float`,
   the result is an infinity of an appropriate sign. If the magnitude
   is too small to represent as a `float`, the result is a
   zero of an appropriate sign.

## Byte Code
```
0x2A
```

## Format
```
divide_d
```

## Operand Stack
**Before**  
```
    ..., value1, value2
```
**After**  
```
    ..., result
```

## Operands
**value1**  
    A `float` value. It is popped off the operand stack.  
**value2**  
    A `float` value. It is popped off the operand stack.  
**result**  
    A `float` value which is the quotient computed by the
    division of `value1` and `value2`, represented as
    `value1 / value2`.