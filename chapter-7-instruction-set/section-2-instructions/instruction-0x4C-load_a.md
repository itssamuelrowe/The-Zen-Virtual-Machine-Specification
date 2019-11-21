# load_a

Load a reference from a local variable.

The `load_a` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x4C
```

## Format
```
load_a index
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The local variable at the index should
    be a reference. This reference is pushed onto the operand stack.

## Operand Stack
**Before**  
```
    ...
```
**After**  
```
    ..., object_reference
```

## Operands
**object_reference**  
    The reference to an object stored at the specified index.
    It is pushed onto the operand stack.