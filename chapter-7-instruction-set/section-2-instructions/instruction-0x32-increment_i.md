# increment_i

Increment a local integer variable.

The `increment_i` instruction can be used in conjunction with the `wide`
mode, in which case the index and constant arguments occupy two bytes each.

## Byte Code
```
0x32
```

## Format
```
increment_i index constant
```

## Arguments
**index**  
    An unsigned byte which is a valid index into the local variable
    array of the current frame. The local variable at the index should
    be a 32-bit integer.  
**constant**  
   A signed byte which is added to the current value of the local
   variable.

## Operand Stack
**Before**  
```
    ...
```
**After**  
```
    ...
```

## Operands
    This instruction does not require any operands.