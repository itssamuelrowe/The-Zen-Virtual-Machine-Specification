# shift_right_i

Bitwise right shift a 32-bit integer value.

Two 32-bit integer operands are popped off the operand stack. A 32-bit
integer result is evaluated by performing a right shift on `value1` by
the number of positions specifiedy by `value2`, shown as
`value1 >> value2`. The shift distance should always be in the range 0
to 31, inclusive.

The result is pushed onto the operand stack.

## Byte Code
```
0x0B
```

## Format
```
shift_right_i
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
    on `value1` by the number of positions specifiedy by `value2`.
