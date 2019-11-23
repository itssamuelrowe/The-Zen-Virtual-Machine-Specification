# load_ad

Load a `double` value from an array.

The value at the specified index is pushed onto the operand stack.

## Byte Code
```
0x67
```

## Format
```
load_ad
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
    A reference to an array whose component type is `double`.
    It is popped off the stack.  
**index**  
    A signed 32-bit integer which indicates the index of the
    component to retrieve. It is popped off the stack.  
**value**  
   A 64-bit `double` value that is stored at the specified index
   in the specified `double` array. It is pushed onto the stack.

## Exceptions
**zen.core.NullPointerException**  
    An instance of the `NullPointerException` class is thrown
    if the specified array is `null`.  
**zen.base.InvalidArrayIndexException**  
    An instance of the `InvalidArrayIndexException` class is
    thrown if the specified index is invalid. An array index is invalid
    if one of the following is true:  
        - Index is negative  
        - Index is greater than or equal to the array size