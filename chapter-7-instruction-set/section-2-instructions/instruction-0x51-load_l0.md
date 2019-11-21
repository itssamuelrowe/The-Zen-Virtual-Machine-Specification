# load_l0

Load a 64-bit integer value from a local variable.

Here, `0` should be a valid index into the local variable array. The local
variable at this index should be a 64-bit integer value. This value
is pushed onto the operand stack.

## Byte Code
```
0x51
```

## Format
```
load_l0
```

## Operand Stack
**Before** 
``` 
    ...
``` 
**After**  
```
    ..., value
```

## Operands
**value**  
    The 64-bit integer value at the specified index in the local
    variable array. It is pushed onto the operand stack.