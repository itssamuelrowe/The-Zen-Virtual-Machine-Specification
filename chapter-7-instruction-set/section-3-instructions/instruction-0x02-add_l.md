# add_l

Add two `long` values.

Two `long` operands are popped off the operand stack. An `long` result is
evaluated by adding both the operands, shown as `value1 + value2`.

If an overflow occurs, the bits of the result is truncated to preserve
only the 64-bits from the Least Significant Bit (LSB).

Further, an overflow never raises an exception.

## Byte Code
```
0x02
```

## Format
```
add_l
```

## Operand Stack
****Before**  
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
    A `long` value. It is popped off the operand stack.  
**value2**  
    A `long` value. It is popped off the operand stack.  
**result**  
    A `long` value which is computed by addition of the specified `long` values.