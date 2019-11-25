# load_instance_field

Load the value stored in an instance field.

Pops the argument from the stack. The value stored in the instance field
is retrieved and pushed onto the operand stack.

## Byte Code
```
0x69
```

## Format
```
load_instance_field index0 index1
```

## Operand Stack
**Before**  
```
    ..., instance_reference
```
**After**  
```
    ..., value
```

## Arguments
**index0**  
    An unsigned byte, along with `index1`, forms a valid index into the
    constant pool where the entry is a `ConstantPoolField` instance.  
**index1**  
    Please refer the documentation for `index0` for more details.

## Operands
**instance_reference**  
    A reference to an instance whose field is to be loaded.
    It is popped off the operand stack. The size is contingent on the
    machine, which is transparent to the binary entity format. The value
    is popped off the operand stack.  
**value**  
    The value stored in the instance field.

## Exception
**zen.core.NullPointerException**  
    An instance of the `NullPointerException` class is thrown
    if the specified instance reference is `null`.