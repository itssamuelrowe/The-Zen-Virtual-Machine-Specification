# load_ab

Load a `byte` or a `boolean` value from an array.

The value at the specified index is pushed onto the operand stack.

This instruction is common to both byte and boolean arrays.
The implementation of the virtual machine is free to choose the
internal representation of the arrays.

## Byte Code
```
0x61
```

## Format
```
load_ab
```

## Operand Stack
**Before**  
```
    ..., array, index
```
**After**  
```
    ..., value
```

## Operands
**array**  
    A reference to an array whose component type is `byte` or
    `boolean`. It is popped off the stack.  
**index**  
    A signed 32-bit integer which indicates the index of the
    component to retrieve. It is popped off the stack.  
**value**  
    A signed 32-bit integer derived by extending the sign bit of the
    8-bit integer value at the specified index.

## Exceptions
**zen.core.NullPointerException**  
    An instance of the `NullPointerException` class is thrown
    if the specified array is `null`.  
**zen.core.InvalidArrayIndexException**  
    An instance of the `InvalidArrayIndexException` class is
    thrown if the specified index is invalid. An array index is invalid
    if one of the following is true:  
        - Index is negative  
        - Index is greater than or equal to the array size
