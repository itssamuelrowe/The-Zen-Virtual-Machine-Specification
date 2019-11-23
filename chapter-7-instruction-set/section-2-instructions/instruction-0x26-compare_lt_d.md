# compare_lt_d

Compare two `double` values.

If at least one of the values is NaN, the pair of values is unordered.
Therefore, in order to prevent failure in comparison of such a pair and
also compute consistent results the `compare_lt_d` instruction
works relatively to the `compare_gt_d` instruction.

## Byte Code
```
0x26
```

## Format
```
compare_lt_d
```

## Operand Stack
**Before**  
```
    ..., value1, value2
```
**After**  
```
    ..., result
```

## Operands
**value1**  
    A `double` value. It is popped off the operand stack.  
**value2**  
    A `double` value. It is popped off the operand stack.  
**result**  
    The result varies contingent on the following cases. It is pushed
    onto the stack.
 * If `value1` is greater than `value2`, then the result is a positive integer value `1`.
 * If `value1` is lesser than `value2`, then the result is a negative integer value `-1`.
 * If `value1` is equal to `value2`, then the result is a neutral integer `0`.
 * For an unordered pair of values, the result is always `-1`.