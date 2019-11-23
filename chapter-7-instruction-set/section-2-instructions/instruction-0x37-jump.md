# jump

Jump to the specified index.

The instruction pointer (IP) of the current frame is updated to the
instruction at the specified index. The control transfers to that
instruction.

## Byte Code
```
0x37
```

## Format
```
jump index0 index1
```

## Arguments
**index0**  
    An unsigned byte, along with `index1` forms an index into the constant
    pool. The instruction at the specified index should be a valid instruction.  
**index1**  
   Please refer the documentation of `index0` for more details.