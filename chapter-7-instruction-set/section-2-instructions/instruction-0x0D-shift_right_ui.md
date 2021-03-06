# shift_right_ui

Bitwise right shift an unsigned 32-bit integer value, with zero extension.

Two 32-bit integer operands are popped off the operand stack. A 32-bit
integer result is evaluated by performing a right shift on `value1` by
the number of positions specifiedy by `value2`, shown as
`value1 >>> value2`. The shift distance should always be in the range 0
to 31, inclusive.

When `value1` is positive and `value2 & 0x1f` is the distance, the
result is `value1 >> value2`. However, if `value1` is negative, the
result is equal to `(value1 >> (value2 & 0x1f)) + (2 << ~(value2 & 0x1f))`.
Adding `(2 << ~(value2 & 0x1f))` cancels the propagated sign bit.

The result is pushed onto the operand stack.

## Byte Code
```
0x0D
```

## Format
```
shift_right_ui
```

## Operand Stack
****Before**  
**  
```
    ..., value1, value2
```
**After**  
```
    ..., result
```

## Operands
**value1**  
    A 32-bit integer value. It is popped off the operand stack.  
**value2**  
    A 32-bit integer value. It is popped off the operand stack.  
**result**  
    A 32-bit integer value which is computed by performing a right shift
    on `value1` by the number of positions specifiedy by `value2`, with
    sign extension.