# load_d

Load a `double` value from a local variable.

The `load_d` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x4B
```

## Format
```
load_d index
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The local variable at the index should
    be a `double`. This reference is pushed onto the operand
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
    The `double` value stored at the specified index. It is
    pushed onto the stack.