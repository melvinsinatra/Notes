
## What It Is and Why It Exists
**Two’s complement** is the standard method computers use to represent **signed integers** (positive and negative) in binary.

It allows **addition, subtraction, and shifting** to work the same way for both positive and negative numbers.

## The Core Idea
For an _N-bit_ integer:
- Positive numbers → normal binary
- Negative numbers →  *invert all bits + add 1*

## How to Represent a Negative Number
### Example: Represent `-5` using 8 bits
1. Start with `+5`
    `00000101`
2. Invert all bits
    `11111010`
3. Add `1`
    `11111011`
So:
`-5 = 11111011 (two’s complement)`