# KRJPLMod DOM Manipulation

## Overview
The KRJPLMod DOM Manipulation system is the most advanced, efficient, and developer-friendly way to interact with the Document Object Model (DOM). It surpasses JavaScript’s native DOM API, jQuery, and other frameworks by providing:

- **Ultra-Fast Virtual DOM with Automatic Reconciliation**
- **Declarative and Intuitive Syntax**
- **Real-Time State Binding**
- **Batch Processing for High Performance**
- **Direct Element Selection & Modification**
- **Event Handling & Custom Listeners**
- **Built-in Animations & Transitions**
- **Seamless WebSocket Integration for Real-Time Updates**

## 1. Selecting Elements
KRJPLMod provides direct element selection using `web.get()`.

```krjplmod
let title = web.get("#title");
```

## 2. Modifying Elements
Change text, attributes, and styles instantly.

```krjplmod
web.set("#title", "Welcome to KRJPLMod!");
web.attr("#title", "class", "main-heading");
web.style("#title", "color: blue; font-size: 24px;");
```

## 3. Creating & Appending Elements
Dynamically add new elements to the DOM.

```krjplmod
let newDiv = web.create("div", "Hello World!");
web.append("#container", newDiv);
```

## 4. Removing Elements
Easily remove unwanted elements from the page.

```krjplmod
web.remove("#oldElement");
```

## 5. Event Handling
Attach event listeners in a declarative manner.

```krjplmod
fn onClick() {
    print("Element clicked!");
}

web.on("#btn", "click", onClick);
```

## 6. Real-Time State Binding
Automatically update the UI when data changes.

```krjplmod
state message = "Hello!";
web.bind("#message", message);

fn updateMessage() {
    message = "Welcome to KRJPLMod!";
}
```

## 7. Animations & Transitions
Apply animations effortlessly with built-in functions.

```krjplmod
web.animate("#box", "fadeIn", 500);
web.transition("#box", "transform: scale(1.2)", 300);
```

## 8. Batch DOM Updates for Performance
Minimize reflows and repaints with batch updates.

```krjplmod
web.batch(fn() {
    web.set("#title", "Updated Title");
    web.style("#title", "color: red;");
});
```

## 9. WebSocket-Driven Dynamic Updates
Integrate real-time data with WebSockets.

```krjplmod
let ws = web.socket("wss://server.com");
ws.on("message", fn (data) {
    web.set("#liveData", data);
});
```

## 10. Shadow DOM & Custom Elements
Encapsulate styles and structure within custom components.

```krjplmod
component Card {
    fn render() -> string {
        return "<div class='card'><slot></slot></div>";
    }
}
```

## Conclusion
KRJPLMod’s DOM Manipulation system is the most powerful and optimized solution for interactive web development. Next, explore [Styling](styling.md) to enhance your applications' appearance.

