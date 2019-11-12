# add_i

Add two `int` values.

Two `int` operands are popped off the operand stack. An `int`
result is evaluated by adding both the operands, shown as `value1 + value2`.

If an overflow occurs, the bits of the result is truncated to preserve
only the 32-bits from the Least Significant Bit (LSB).

Further, an overflow never raises an exception.

## Byte Code
```
0x01
```

## Format
```
add_i
```

## Operand Stack
******Before**  
**  
**  
```
    ..., value1, **value2**  
```

****After**  
**
```
    ..., **result**  
```

## Operands
**value1**  
    A `int` value. It is popped off the operand stack.  
**value2**  
    A `int` value. It is popped off the operand stack.  
**result**  
    A `int` value which is computed by addition of the specified `int` values.