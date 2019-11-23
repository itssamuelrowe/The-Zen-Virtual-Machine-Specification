# load_aa

Load a reference from a reference array.

Pops both the arguments from the stack. The element at the specified
index is retrieved and pushed onto the operand stack.

## Byte Code
```
0x68
```

## Format
```
load_aa
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

## Arguments
**array**  
    A reference to the array whose component type is `reference`.  
**index**  
    The index of the element to retrieve.

## Exceptions
**zen.core.NullPointerException**  
    An instance of the `NullPointerException` class is thrown
    if the specified array is `null`.  
**zen.base.InvalidArrayIndexException**  
    An instance of the `InvalidArrayIndexException` class is
    thrown if the specified index is invalid.