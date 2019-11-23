# invoke_special

Invoke a special function such as constructor.

A new frame is created on the virtual machine stack for the function
being invoked. The instance reference and arguments are consecutively
stored in the local variable array of the new frame. The instance reference
stored at index `0`, `argument1` at `1`, `argument2` at `2` and so on.

It should be noted that in the case of values such `long` and `double`,
two indexes are occupied. Because the reference type depends on the platform,
it may occupy one or two indexes. This is transparent to the binary entity.

After the new frame is initialized, it is promoted as the current frame.
The instruction pointer (IP) of the current frame is initialized to the
first instruction of the invoked function.

## Byte Code
```
0x33
```

## Format
```
invoke_special index0 index1
```

## Arguments
**index0**  
    An unsigned byte, along with `index1` forms an index into the constant
    pool. The entry at the specified index should be a `ConstantPoolFunction`
    instance.  
**index1**  
   Please refer the documentation of `index0` for more details.

## Operand Stack
**Before**
```
    ..., instance_reference, [argument1, [argument2, ...]]
```
**After**
```
    ...
```

## Operands
**instance_reference**  
    A reference to an instance whose special function is to be invoked.
    It is popped off the operand stack. The size is contingent on the
    machine, which is transparent to the binary entity format. The value
    is popped off the operand stack.  
**argument1, argument2, ...**  
    The arguments passed to the special function. The signature of the
    function determines the number of operands popped off the operand
    stack as arguments.  
**result**  
    This instruction does not generate any result.

## Exceptions
**NullPointerException**  
    If the instance reference is `null`, this instruction causes the
    virtual machine to throw a `zen.core.NullPointerException`.