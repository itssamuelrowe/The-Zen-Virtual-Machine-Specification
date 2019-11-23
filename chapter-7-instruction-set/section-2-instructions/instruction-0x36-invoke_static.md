# invoke_static

Invoke a static function.

If the function is not native, a new frame is created on the virtual
machine stack for the function being invoked. The arguments are consecutively
stored in the local variable array of the new frame. `argument1` at `1`,
`argument2` at `2` and so on.

After the new frame is initialized, it is promoted as the current frame.
The instruction pointer (IP) of the current frame is initialized to the
first instruction of the invoked function.

If the function returns a value, the value is pushed onto the operand
stack of the previous stack frame.

If the function is native, a new frame is created on the virtual
machine stack for the function being invoked. The arguments are consecutively
stored in the local variable array of the new frame. `argument1` at `1`,
`argument2` at `2` and so on.

If the native function returns a value, the platform dependent return
value is converted to an implementation dependent value. The new value is
then pushed onto the operand stack of the previous stack frame.

It should be noted that in the case of values such `long` and `double`,
two indexes are occupied. Because the reference type depends on the platform,
it may occupy one or two indexes. This is transparent to the binary entity.

## Byte Code
```
0x36
```

## Format
```
invoke_static index0 index1
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
    ..., [argument1, [argument2, ...]]
```
**After**
```
    ...
```

## Operands
**argument1, argument2, ...**  
    The arguments passed to the static function. The signature of the
    function determines the number of operands popped off the operand
    stack as arguments.  
**result**  
    This instruction does not generate any result.

## Exceptions
**UndefinedNativeFunctionError**  
    If a native function is invoked and the virtual machine is not able
    to find its definition, this instruction causes the virtual machine
    to throw a `zen.core.UndefinedNativeFunctionError`.