# invoke_virtual

Invoke a function against an instance.

## Byte Code
```
0x34
```

## Format
```
invoke_virtual index0 index1
```

## Operand Stack
**Before**  
```
    ..., object_reference, [argument_1, [argument_2, [argument_3, ...]]]
```
**After**  
```
    ...
```

## Operands
**index_byte_1**  
    The `index0` and `index1` bytes together indicate an unsigned integer
    index into the runtime constant pool of the current binary entity.
    The item at this index represents a function descriptor.  
**index_byte_2**  
    Please refer the documentation for `index0`.
