# load_static_field

Load the value stored in a static field.

Pops the argument from the stack. The value stored in the static field
is retrieved and pushed onto the operand stack.

## Byte Code
```
0x6A
```

## Format
```
load_static_field index0 index1
```

## Operand Stack
**Before**  
```
    ...
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
**value**  
    The value stored in the static field.