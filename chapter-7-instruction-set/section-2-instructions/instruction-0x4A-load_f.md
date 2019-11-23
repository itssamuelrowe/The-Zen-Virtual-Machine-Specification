# load_f

Load a `float` value from a local variable.

The `load_f` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x4A
```

## Format
```
load_f index
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The local variable at the index should
    be a `float`. This value is pushed onto the operand
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
    The `float` value stored at the specified index. It is
    pushed onto the stack.