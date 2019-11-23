# load_f3

Load a `float` value from a local variable.

Here, 3 should be a valid index into the local variable array. The local
variable at this index should be a `float` value. This reference
is pushed onto the operand stack.

## Byte Code
```
0x58
```

## Format
```
load_f3
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
    The `float` value at the specified index in the local
    variable array. It is pushed onto the operand stack.