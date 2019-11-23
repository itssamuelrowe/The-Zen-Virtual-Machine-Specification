# load_l

Load a 64-bit integer value from a local variable.

The `load_l` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x49
```

## Format
```
load_l index
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The values at `index` and `index + 1`
    are combined to construct a 64-bit integer value. This value is
    pushed onto the operand stack.

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
    The 64-bit integer value constructed with the values stored at
    `index` and `index + 1`. It is pushed onto the stack.