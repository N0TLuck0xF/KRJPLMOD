# Functions in KRJPLMod

## Overview
Functions in KRJPLMod allow code reuse and modular programming. They support parameters, return values, and can be structured as standard functions or anonymous (lambda) functions.

## 1. Declaring Functions
Functions are defined using the `fn` keyword and can optionally return values.

```krjplmod
fn greet(name: string) -> string {
    return "Hello, " + name;
}

let message = greet("John");
print(message); // Output: Hello, John
```

## 2. Function Parameters
Functions can accept multiple parameters with type annotations.

```krjplmod
fn add(a: int, b: int) -> int {
    return a + b;
}

print(add(5, 10)); // Output: 15
```

## 3. Default Parameters
Default values can be assigned to parameters.

```krjplmod
fn welcome(name: string = "Guest") {
    print("Welcome, " + name);
}

welcome(); // Output: Welcome, Guest
welcome("Alice"); // Output: Welcome, Alice
```

## 4. Anonymous (Lambda) Functions
KRJPLMod supports inline functions for concise operations.

```krjplmod
let multiply = |x: int, y: int| -> int {
    return x * y;
};

print(multiply(3, 4)); // Output: 12
```

## 5. Higher-Order Functions
Functions can accept other functions as arguments or return functions.

```krjplmod
fn apply_twice(func: fn(int) -> int, value: int) -> int {
    return func(func(value));
}

fn square(x: int) -> int {
    return x * x;
}

print(apply_twice(square, 2)); // Output: 16
```

## 6. Recursive Functions
Functions can call themselves for tasks like factorial calculation.

```krjplmod
fn factorial(n: int) -> int {
    if n <= 1 {
        return 1;
    }
    return n * factorial(n - 1);
}

print(factorial(5)); // Output: 120
```

## 7. Closures
Functions can capture variables from their enclosing scope.

```krjplmod
fn counter() -> fn() -> int {
    mut count = 0;
    return || -> int {
        count += 1;
        return count;
    };
}

let next = counter();
print(next()); // Output: 1
print(next()); // Output: 2
```

## Conclusion
Functions in KRJPLMod provide a flexible and powerful way to structure programs. Next, explore [Loops & Iteration](loops.md) to understand flow control in KRJPLMod.

