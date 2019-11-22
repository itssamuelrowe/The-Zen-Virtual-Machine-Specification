# Instruction Nomenclature

## Format
```
name_[_modifier_][wide][array][sign][primitive_type][index]
```

**Modifier**  
A modifier is local to the instruction. It indicates the modified primary
operation the instruction performs. This part is rarely seen in the ZVM
instruction set.

**Wide**  
An instruction may have an extended version where the size of one or more
input data is wider than the normal version. Such instructions are marked
with 'w'.

**Array**  
An instruction which operates on one or more array references is marked
with 'a'.

**Sign**  
Albeit the ZVM does not support unsigned integers in general, certain
instructions interpret signed and unsigned properties of an integer value.
Such instructions are marked with one of the following characters:  
's' - signed (This marker is usually omitted.)  
'u' - unsigned  

**Primitive Types**  
Certain instructions have multiple version which operate exclusively on
a primitive type. Such instructions are marked with one of the following
characters:  
'b' - byte  
's' - short  
'i' - integer  
'l' - long  
'f' - float  
'd' - double  
'a' - reference  

**Index**  
Certain instructions operate on data at a specified index. The meaning of
the index is local to the instruction in question. In order to enhance the
performance of the virtual machine, these instructions usually have hybrid
versions which operate on predefined indexes. Such instructions are marked
with {@code 0} or any of the positive integers.

## Examples  

> NOTE: These instructions are completely imaginary and have no special
> meaning to the virtual machine. They are here merely to help the
> reader understand the nomenclature.

```
name_wad0
name_0
name_as
name_i0
```
