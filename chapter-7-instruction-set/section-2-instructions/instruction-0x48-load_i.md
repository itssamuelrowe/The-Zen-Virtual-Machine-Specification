# load_i

Load a 32-bit integer value from a local variable.

The `load_i` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x48
```

## Format
```
load_i index
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The local variable at the index should
    be a 32-bit integer value. This value is pushed onto the operand
    stack.

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
    The 32-bit integer value stored at the specified index. It is
    pushed onto the stack.