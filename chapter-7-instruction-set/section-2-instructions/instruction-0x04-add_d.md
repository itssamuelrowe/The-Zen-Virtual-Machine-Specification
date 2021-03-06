# add_d

Add two `double` values.

The following rules, as specified by IEEE 754, should be observed when
adding two `double` values.
* If either the first or the second operand is NaN, the result is
  always NaN.
* The sum of two infinities of opposite sign is NaN.
* The sum of two infinities of the same sign is the infinity of
  the sign in question.
* The sum of an infinity and any finite value is infinity.
* The sum of two zeroes of opposite sign is positive zero.
* The sum of two zeroes of the same sign is the zero of the sign
  in question.
* The sum of a zero and a non-zero finite value is the non-zero
  value.
* The sum of two non-zero finite values of the same magnitude and
  opposite sign is positive zero.
* In the remaining cases, where neither operand is an infinity, a
  zero, or NaN and the values have the same sign or have different
  magnitudes, the sum is computed and rounded to the nearest
  representable value using IEEE 754 round to nearest mode. If
  the magnitude is too large to represent as a `double`,
  the result is an infinity of an appropriate sign. If the magnitude
  is too small to represent as a `double`, the result is a
  zero of an appropriate sign.

## Byte Code
```
0x04
```

## Format
```
add_d
```

## Operand Stack
******Before**  
**  
**  
```
    ..., value1, value2
```
****After**  
**  
```
    ..., result
```

## Operands
**value1**  
    A `double` value. It is popped off the operand stack.  
**value2**  
    A `double` value. It is popped off the operand stack.  
**result**  
    A `double` value which is computed by addition of the specified `double` values.