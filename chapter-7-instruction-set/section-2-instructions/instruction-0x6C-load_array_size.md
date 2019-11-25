# load_array_size

Load the size of an array.

Pops the argument from the stack. The size of the array is retrieved
and pushed onto the operand stack.

## Byte Code
```
0x6C
```

## Format
```
load_array_length
```

## Operand Stack
**Before**  
```
    ..., array
```
**After**  
```
    ..., value
```

## Operands
**array**  
    A reference to an array whose size is to be loaded.
    It is popped off the operand stack. The size is contingent on
    the machine, which is transparent to the binary entity format.
    The value is popped off the operand stack.  
**value**  
    The size of the array.

## Exception
**zen.core.NullPointerException**  
    An instance of the `NullPointerException` class is thrown
    if the specified array is `null`.