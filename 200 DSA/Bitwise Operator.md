
## Number as binary code examples
- 1: 00000001
- 2: 00000010

Bitwise operators are operators that work on the individual binary digits
## Bitwise Operator Examples

### 1. Bitwise OR
= Compare the digits of two or more variables. If either digit is "1", then the result would be "1". Else, the result would be "0".
- 1: 00000001
- 2: 00000010
- R: 00000011
```javascript
console.log(1 | 2) // Bitwise OR. Result is 00000011 (3 in binary)
console.log(1 | 2 | 3)
```

### 2. Bitwise AND
= Compare the digits of two or more variables. If both digit is "1", then the result would be "1". Else, the result would be "0".
- 1: 00000001
- 2: 00000010
- R: 00000000
```javascript
console.log(1 *|* 2) // Bitwise AND. Result is 00000000
```

### 3. Shift Right Operator
- Shifts bits to the right by `n` position
- Bits shifted out on the right are discarded
- For *[[Signed integers]]*, the leftmost bit is filled with the sign bit (arithmetic shift)

Simple example
```javascript
let x = 8 //binary: 1000
let y = x >> 1 //binary: 0100

console.log(y); // 4

let a = 7 //binary: 0111
let b = a >> 1 //binary: 0011

console.log(b); // 3
// This matches integer devision:
// 7 / 2 = 3
```


## Real World Use Cases

### 1. Check if a number is even or odd
```
num & 1
```
- 0 -> even
- 1 -> odd