# cast_lti

Convert a 64-bit integer value to a 32-bit integer value.

The instruction narrows the 64-bit integer value. Therefore, loss of
information in regards to magnitude and precision may be observed.

In other words, the 64-bit integer is truncated to 32-bit integer, then
the sign is extended to a 32-bit result.

## Format
```
cast_lti
```

## Operand Stack
**Before**  
```
    ..., value
```
**After**  
```
    ..., result
```

## Operands
**value**  
    A 64-bit integer value. It is popped off the operand stack.  
**result**  
    A 32-bit integer` value derived from converting the specified
    64-bit integer value to 32-bit integer value. The sign is extended to
    a 32-bit integer before it is pushed onto the operand stack.
