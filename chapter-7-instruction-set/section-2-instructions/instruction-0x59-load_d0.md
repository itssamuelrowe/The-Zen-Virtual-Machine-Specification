# load_d0

Load a `double` value from a local variable.

Here, 0 should be a valid index into the local variable array. The local
variable at this index should be a `double` value. This reference
is pushed onto the operand stack.

## Byte Code
```
0x59
```

## Format
```
load_d0
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
    The `double` value at the specified index in the local
    variable array. It is pushed onto the operand stack.