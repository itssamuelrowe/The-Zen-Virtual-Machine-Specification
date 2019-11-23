# load_a0

Load a reference from a local variable. Here, 0 should be a valid index
into the local variable array. The local variable at this index should
be a reference. This reference is pushed onto the operand stack.

## Byte Code
```
0x5D
```

## Format
```
load_a0
```

## Operand Stack
**Before**  
```
    ...
```
**After**  
```
    ..., object_reference
```