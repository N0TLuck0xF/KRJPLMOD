# KRJPLMod Syntax & Structure

## Overview
KRJPLMod follows a structured and readable syntax that blends elements of Python, JavaScript, and Rust, ensuring efficiency in web, game, and AI development.

## 1. Variables & Data Types
KRJPLMod supports statically and dynamically typed variables.

### **Variable Declaration**
```krjplmod
let x = 10;  // Immutable variable
mut y = 20;  // Mutable variable
```

### **Data Types**
- `int` - Integer numbers
- `float` - Floating-point numbers
- `bool` - Boolean values (`true` / `false`)
- `string` - Text values
- `array` - Lists of elements
- `map` - Key-value storage

## 2. Functions
Functions can be declared with or without return types.
```krjplmod
fn greet(name: string) -> string {
    return "Hello, " + name;
}
```

## 3. Conditionals
Conditional statements use standard `if`, `elif`, and `else` syntax.
```krjplmod
if x > 10 {
    print("X is greater than 10");
} elif x == 10 {
    print("X is 10");
} else {
    print("X is less than 10");
}
```

## 4. Loops
### **For Loop**
```krjplmod
for i in range(0, 5) {
    print(i);
}
```
### **While Loop**
```krjplmod
mut count = 0;
while count < 5 {
    print(count);
    count += 1;
}
```

## 5. Classes & Objects
KRJPLMod supports object-oriented programming with classes and constructors.
```krjplmod
class Person {
    mut name: string;
    
    fn init(name: string) {
        self.name = name;
    }
    
    fn greet() {
        print("Hello, " + self.name);
    }
}

let p = Person("John");
p.greet();
```

## 6. Modules & Imports
Modules help in organizing code.
```krjplmod
import math;
let result = math.sqrt(25);
print(result);
```

## 7. Error Handling
```krjplmod
try {
    let num = 10 / 0;
} catch e {
    print("Error: " + e.message);
}
```

## 8. Web & Database Integration
KRJPLMod provides built-in support for web APIs and databases.
```krjplmod
http.get("https://api.example.com/data");
db.connect("my_database");
```

## Conclusion
KRJPLMod is a powerful and expressive language optimized for modern development needs. Next, explore [Functions & Advanced Features](functions.md) to deepen your understanding.

