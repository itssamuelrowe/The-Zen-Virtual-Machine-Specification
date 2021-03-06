# xor_l

Bitwise Exclusive OR (XOR) of two 64-bit integer values.

Two 64-bit integer operands are popped off the operand stack. A 64-bit
integer result is evaluated by performing an exclusive conjunction
(bitwise XOR) of both the operands, shown as value1 ^ value2`.

The result is pushed onto the operand stack.

## Byte Code
```
0x10
```

## Format
```
xor_l
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
    A 64-bit integer value. It is popped off the operand stack.  
**result**  
    A 64-bit integer value which is computed by performing an exclusive
    conjunction (bitwise XOR) of both the specified 64-bit integer values.
