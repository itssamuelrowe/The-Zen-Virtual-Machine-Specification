# load_as

Load a 16-bit integer value from an array.

The value at the specified index is pushed onto the operand stack.

## Byte Code
```
0x63
```

## Format
```
load_as
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
    A reference to an array whose component type is `short`.
    It is popped off the stack.  
**index**  
    A signed 32-bit integer which indicates the index of the
    component to retrieve. It is popped off the stack.  
**value**  
    A signed 32-bit integer derived by extending the sign bit of the
    16-bit integer value at the specified index.

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