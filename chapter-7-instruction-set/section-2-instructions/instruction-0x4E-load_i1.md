# load_i1

Load a 32-bit integer value from a local variable.

Here, `1` should be a valid index into the local variable array. The local
variable at this index should be a 32-bit integer value. This value
is pushed onto the operand stack.

## Byte Code
```
0x4E
```

## Format
```
load_i1
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
    The 32-bit integer value at the specified index in the local
    variable array. It is pushed onto the operand stack.