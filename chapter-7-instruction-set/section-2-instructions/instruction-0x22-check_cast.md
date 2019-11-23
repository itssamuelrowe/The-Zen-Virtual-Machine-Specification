# check_cast

Check whether an object is an instance of a type.

The operand stack remains unchanged in the following cases:
 * CASE 1: The specified reference is `null`.
 * CASE 2: The object can be cast to the specified class, enumeration, or array type.
Otherwise, an instance of the `ClassCastException` class is
thrown.

## Byte Code
```
0x22
```

## Format
```
check_cast index_byte_1 index_byte_2
```

## Arguments
**index_byte_1**  
    The `index_byte_1` and `index_byte_2` together indicate
    an unsigned integer index into the run-time constant pool of the
    current binary entity. The item at this index represents a reference
    to a class, an enumeration, or an array type.
**index_byte_2**  
    Please refer the documentation for `index_byte_1`.

## Operand Stack
**Before**  
```
    ..., object_reference
```
**After**  
```
    ..., object_reference
```

## Operands
object_reference
    A reference to the object to cast.

## Exception
**Resolution Exceptions**  
    During resolution of the class, enumeration, or array types, any of
    the documented exceptions for type resolution may be thrown.  
**zen.base.ClassCastException**  
    An instance of the `ClassCastException` class is thrown
    if the specified object cannot be cast to the specified type.
