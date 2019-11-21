# load_l2

Load a 64-bit integer value from a local variable.

Here, `2` should be a valid index into the local variable array. The local
variable at this index should be a 64-bit integer value. This value
is pushed onto the operand stack.

## Byte Code
```
0x53
```

## Format
```
load_l2
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