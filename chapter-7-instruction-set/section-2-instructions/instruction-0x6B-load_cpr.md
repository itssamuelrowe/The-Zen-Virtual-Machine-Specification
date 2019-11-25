# load_cpr

Load an item from the constant pool.

The `load_cpr` instruction can be used in conjunction with the `wide`
mode, in which case the index occupies two bytes.

## Byte Code
```
0x6B
```

## Format
```
load_cpr index
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

## Arguments
**index**  
    An unsigned 8-bit integer which indicates the index of the
    item in the constant pool.

## Operands
**value**  
    The value of the item is pushed onto the operand stack.