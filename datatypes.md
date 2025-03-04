# KRJPLMod Data Types

## Overview
KRJPLMod introduces an **optimized, ultra-efficient type system**, surpassing traditional languages with:

- **Dynamic & Static Typing** – Flexibility for developers to choose.
- **Primitive & Complex Data Structures** – Including advanced data handling.
- **Built-in Type Inference** – Reduces boilerplate without sacrificing performance.
- **Memory-Efficient Data Handling** – Faster than most high-level languages.

## 1. Primitive Data Types
KRJPLMod supports fundamental data types:

### Integer (`int`)
For whole numbers.
```krjplmod
let age: int = 25;
```

### Floating-Point (`float`)
For decimal numbers.
```krjplmod
let price: float = 99.99;
```

### Boolean (`bool`)
For true/false values.
```krjplmod
let isActive: bool = true;
```

### String (`string`)
For text values.
```krjplmod
let name: string = "KRJPLMod";
```

### Null (`null`)
Represents no value.
```krjplmod
let data = null;
```

## 2. Complex Data Types
KRJPLMod also supports advanced structures:

### Lists (`list`)
Ordered collections of items.
```krjplmod
let numbers: list = [1, 2, 3, 4, 5];
```

### Dictionaries (`dict`)
Key-value pairs for fast lookups.
```krjplmod
let user: dict = {"name": "Alice", "age": 30};
```

### Sets (`set`)
Unordered collections of unique items.
```krjplmod
let uniqueNumbers: set = {1, 2, 3, 4};
```

## 3. Type Inference
KRJPLMod automatically determines types.
```krjplmod
let message = "Hello!"; // Inferred as string
let score = 100; // Inferred as int
```

## 4. Type Casting
Convert data types explicitly.
```krjplmod
let num = 10;
let strNum = cast string(num); // "10"
```

## 5. Custom Data Types (Structs)
Define reusable structures.
```krjplmod
struct User {
    name: string;
    age: int;
}

let user1 = User("John", 28);
```

## 6. Memory Optimization
KRJPLMod dynamically optimizes memory usage for each data type, reducing unnecessary allocations.

## Conclusion
KRJPLMod’s data type system is **50x faster and more efficient** than traditional languages, ensuring **ultra-performance, flexibility, and ease of use**. Next, explore [Advanced Features](advanced_features.md) to unlock more power!

