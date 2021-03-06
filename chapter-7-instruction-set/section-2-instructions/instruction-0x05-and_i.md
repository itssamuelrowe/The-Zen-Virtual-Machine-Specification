# and_i

Bitwise AND of two 32-bit integer values.

Two 32-bit integer operands are popped off the operand stack. A 32-bit
integer result is evaluated by performing a conjunction (bitwise AND)
of both the operands, shown as `value1 & value2`.

The result is pushed onto the operand stack.

## Byte Code
```
0x05
```

## Format
```
add_i
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
    A 32-bit integer value which is computed by performing a conjunction
    of both the specified 32-bit integer values.
