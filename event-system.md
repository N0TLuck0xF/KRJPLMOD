# KRJPLMod Event System

## Overview
KRJPLMod introduces the **most powerful event system**, surpassing JavaScript, React, and other frameworks with:

- **Ultra-Fast Event Binding** – Directly binds to elements for near-instant execution.
- **Declarative & Procedural Event Handling** – Supports both inline and function-based handlers.
- **Global & Local Event Listeners** – Capture and manage events across the entire app.
- **Asynchronous Event Flow** – Supports async/await within event handlers.
- **Custom Event System** – Developers can define custom events for components.

## 1. Basic Event Binding
KRJPLMod simplifies event binding with `on:event` syntax.

```krjplmod
web.render("#app", "<button on:click='sayHello'>Click Me</button>");

fn sayHello() {
    print("Hello, KRJPLMod!");
}
```

## 2. Inline Event Handlers
You can define event logic directly within the HTML structure.

```krjplmod
web.render("#app", "<button on:click='print(\"Button Clicked!\")'>Press</button>");
```

## 3. Handling Keyboard Events
Capture user input efficiently.

```krjplmod
web.render("#app", "<input id='textInput' on:keyup='handleKey' />");

fn handleKey(event) {
    print("Key Pressed: " + event.key);
}
```

## 4. Asynchronous Event Handling
KRJPLMod allows event handlers to be asynchronous.

```krjplmod
web.render("#app", "<button on:click='fetchData'>Load Data</button>");

async fn fetchData() {
    let data = await web.fetch("https://api.example.com/data");
    print(data);
}
```

## 5. Global Event Listeners
Capture events across the entire application.

```krjplmod
web.on("resize", fn () {
    print("Window Resized!");
});
```

## 6. Custom Events & Dispatching
Define and trigger custom events between components.

```krjplmod
web.createEvent("customAlert");

fn triggerAlert() {
    web.dispatch("customAlert", "This is a custom event!");
}

web.on("customAlert", fn (message) {
    print("Received: " + message);
});
```

## 7. Event Delegation
Efficient event handling for dynamically generated elements.

```krjplmod
web.delegate(".list-item", "click", fn (event) {
    print("Clicked on: " + event.target.text);
});
```

## 8. Prevent Default & Stop Propagation
Control event behavior to prevent unintended actions.

```krjplmod
fn handleClick(event) {
    event.preventDefault();  // Stops default action
    event.stopPropagation(); // Stops event bubbling
}
```

## Conclusion
KRJPLMod’s event system is designed for **maximum performance, flexibility, and ease of use**. Next, explore [State Management](state-management.md) to handle application data efficiently.

