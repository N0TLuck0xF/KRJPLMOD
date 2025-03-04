# KRJPLMod Web Framework

## Overview
The KRJPLMod Web Framework is a cutting-edge, built-in framework designed to create dynamic, high-performance web applications. It surpasses existing frameworks like React, Vue, and Svelte by offering a fully integrated development experience with:

- **Declarative Component-Based UI**
- **Reactive State Management**
- **Server-Side Rendering (SSR) & Static Site Generation (SSG)**
- **Full DOM Manipulation Support**
- **Built-in Routing System**
- **Seamless WebSocket Integration for Real-Time Apps**
- **CSS-Like Styling & Theming**
- **Optimized Performance with Virtual DOM**

## 1. Installation & Setup
The framework is included with KRJPLMod, so no external dependencies are needed. Simply import the core module:

```krjplmod
import web;
```

## 2. Creating Components
Components are the building blocks of KRJPLMod web applications. They can be defined using the `component` keyword.

```krjplmod
component Button {
    prop text: string;
    fn render() -> string {
        return "<button onclick='clickHandler()'>" + text + "</button>";
    }
}
```

## 3. Rendering Components
Use `web.render()` to mount components to the DOM.

```krjplmod
let btn = Button("Click Me");
web.render(btn, "#app");
```

## 4. Reactive State Management
KRJPLMod provides a built-in reactive state system.

```krjplmod
state count = 0;

fn increment() {
    count += 1;
}

web.bind("#counter", count);
```

## 5. Event Handling
Event listeners can be attached directly to elements.

```krjplmod
fn onClick() {
    print("Button clicked!");
}

web.on("button", "click", onClick);
```

## 6. Dynamic DOM Manipulation
Modify the DOM dynamically using built-in methods.

```krjplmod
web.set("#title", "New Title");
web.addClass("#title", "highlight");
```

## 7. Routing System
Define routes with `web.route()`.

```krjplmod
web.route("/", HomePage);
web.route("/about", AboutPage);

web.start();
```

## 8. Server-Side Rendering (SSR)
For better performance and SEO, components can be pre-rendered on the server.

```krjplmod
web.ssr("/home", HomePage);
```

## 9. WebSockets for Real-Time Apps
Use `web.socket()` for WebSocket-based applications.

```krjplmod
let ws = web.socket("wss://server.com");

ws.on("message", fn (data) {
    print("Received: " + data);
});
```

## 10. CSS-Like Styling System
Define styles with `web.style()`.

```krjplmod
web.style("button", "background: blue; color: white; padding: 10px;");
```

## Conclusion
The KRJPLMod Web Framework provides an all-in-one solution for web development, ensuring optimal performance, scalability, and developer experience. Next, explore [GUI Library](gui-library.md) for desktop application development.

