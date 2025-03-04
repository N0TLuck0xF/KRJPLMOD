# Loops & Iteration in KRJPLMod

## Overview
Loops in KRJPLMod allow repeated execution of code blocks. The language supports `for` loops, `while` loops, and `loop` constructs for iteration.

## 1. For Loops
The `for` loop iterates over a range, array, or iterable object.

### **Iterating Over a Range**
```krjplmod
for i in range(0, 5) {
    print(i);
}
// Output: 0 1 2 3 4
```

### **Iterating Over an Array**
```krjplmod
let numbers = [10, 20, 30, 40];
for num in numbers {
    print(num);
}
// Output: 10 20 30 40
```

## 2. While Loops
The `while` loop executes a block of code as long as a condition is true.

```krjplmod
mut count = 0;
while count < 5 {
    print(count);
    count += 1;
}
// Output: 0 1 2 3 4
```

## 3. Infinite Loops with `loop`
The `loop` keyword creates an infinite loop, which can be exited using `break`.

```krjplmod
mut x = 0;
loop {
    print(x);
    x += 1;
    if x == 5 {
        break;
    }
}
// Output: 0 1 2 3 4
```

## 4. Loop Control Statements
KRJPLMod supports `break` and `continue` for loop control.

### **Break Statement**
Exits the loop immediately.
```krjplmod
for i in range(1, 10) {
    if i == 5 {
        break;
    }
    print(i);
}
// Output: 1 2 3 4
```

### **Continue Statement**
Skips the current iteration and proceeds to the next one.
```krjplmod
for i in range(1, 6) {
    if i == 3 {
        continue;
    }
    print(i);
}
// Output: 1 2 4 5
```

## Conclusion
Loops in KRJPLMod provide flexibility in iteration, supporting ranges, collections, and conditional execution. Next, explore [Classes & Objects](classes.md) to understand object-oriented programming in KRJPLMod.

