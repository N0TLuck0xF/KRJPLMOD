# KRJPLMod Component System

## Overview
KRJPLMod introduces the **most advanced** component-based UI system, surpassing React, Vue, and Svelte with:

- **True Zero-Virtual-DOM Rendering** – Eliminates diffing overhead for instant updates.
- **Real-Time Reactive Components** – Automatic UI updates without extra state management.
- **Server-Side & Client-Side Harmony** – Components work seamlessly on both ends.
- **Built-in Scoped Styling** – Style components without conflicts.
- **Optimized for Web, GUI, and Embedded Systems** – Single framework for all platforms.

## 1. Defining Components
KRJPLMod components are ultra-lightweight and reactive.

```krjplmod
component Button {
    prop text = "Click Me";
    fn render() -> string {
        return "<button class='btn'>" + text + "</button>";
    }
}
```

## 2. Using Components
Components can be embedded seamlessly.

```krjplmod
let myButton = Button("text": "Submit");
web.render("#app", myButton);
```

## 3. Component State & Reactivity
KRJPLMod provides automatic reactivity with minimal code.

```krjplmod
component Counter {
    state count = 0;
    
    fn increment() {
        count += 1;
    }
    
    fn render() -> string {
        return "<div><button on:click='increment'>+1</button> Count: " + count + "</div>";
    }
}
```

## 4. Nested Components
Create complex UIs by nesting components.

```krjplmod
component Card {
    prop title = "Default Title";
    prop content = "Lorem ipsum";
    
    fn render() -> string {
        return "<div class='card'><h3>" + title + "</h3><p>" + content + "</p></div>";
    }
}
```

```krjplmod
let myCard = Card("title": "KRJPLMod is Here!", "content": "This is the best UI framework.");
web.render("#app", myCard);
```

## 5. Scoped & Dynamic Styling
Each component can have its own isolated styling.

```krjplmod
component Badge {
    prop label = "New";
    fn render() -> string {
        return "<span class='badge'>" + label + "</span>";
    }
    
    web.style(".badge", "background: red; color: white; padding: 5px 10px; border-radius: 5px;");
}
```

## 6. Lifecycle Hooks
KRJPLMod provides hooks for fine-grained control over component behavior.

```krjplmod
component Loader {
    fn onMount() {
        print("Component Mounted!");
    }
    
    fn render() -> string {
        return "<div>Loading...</div>";
    }
}
```

## 7. Server-Side Rendering (SSR) & Hydration
KRJPLMod components can render on the server and hydrate on the client.

```krjplmod
web.ssr("#app", myComponent);
```

## Conclusion
KRJPLMod’s component system delivers unparalleled speed, flexibility, and simplicity, making it the ultimate choice for building UI-driven applications. Next, explore [Event System](event-system.md) to handle user interactions efficiently.

