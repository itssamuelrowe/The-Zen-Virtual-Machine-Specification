# shift_right_l

Bitwise right shift a 64-bit integer value.

Two 64-bit and 32-bit integer operands are popped off the operand stack.
A 64-bit integer result is evaluated by performing a right shift on `value1`
by the number of positions specifiedy by `value2`, shown as
`value1 >> value2`. The shift distance should always be in the range 0
to 63, inclusive.

The result is pushed onto the operand stack.

## Byte Code
```
0x0C
```

## Format
```
shift_right_l
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
    A 64-bit integer value. It is popped off the operand stack.  
**value2**  
    A 32-bit integer value. It is popped off the operand stack.  
**result**  
    A 64-bit integer value which is computed by performing a right shift
    on `value1` by the number of positions specifiedy by `value2`.