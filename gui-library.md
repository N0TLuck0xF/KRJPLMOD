# KRJPLMod GUI Library

## Overview
The KRJPLMod GUI Library is a powerful yet lightweight graphical user interface (GUI) framework designed for building cross-platform desktop applications with high performance. It surpasses Tkinter, Electron, and other GUI frameworks by offering:

- **Lightweight and Fast Rendering**
- **Component-Based UI System**
- **Reactive State Management**
- **Native-Like Performance Without Bloat**
- **Cross-Platform Support (Windows, Linux, macOS)**
- **Seamless Integration with Web & KRJPLMod Apps**
- **Built-in Theming & CSS-Like Styling**

## 1. Installation & Setup
KRJPLMod’s GUI library is built-in, requiring no additional dependencies. Simply import the core module:

```krjplmod
import gui;
```

## 2. Creating Windows & UI Elements
Windows and UI elements are created using the `Window` and `Element` classes.

```krjplmod
let win = gui.Window("My App", 800, 600);

let btn = gui.Button("Click Me");
win.add(btn);
win.show();
```

## 3. Event Handling
Attach event listeners directly to UI elements.

```krjplmod
fn onClick() {
    print("Button clicked!");
}

btn.on("click", onClick);
```

## 4. Layout & Positioning
KRJPLMod’s GUI library supports flexible layout management.

```krjplmod
win.layout("grid");
win.add(gui.Label("Welcome!"), row=0, col=0);
win.add(btn, row=1, col=0);
```

## 5. Reactive State Management
UI components automatically update when state changes.

```krjplmod
state counter = 0;
let lbl = gui.Label(counter);

fn increment() {
    counter += 1;
}

btn.on("click", increment);
```

## 6. Native File Dialogs & Notifications
Built-in dialogs and notifications for seamless user interaction.

```krjplmod
let file = gui.openFileDialog();
gui.notify("File Selected: " + file);
```

## 7. CSS-Like Styling System
Define styles globally or per element.

```krjplmod
gui.style("button", "background: blue; color: white; padding: 10px;");
```

## 8. Theming & Dark Mode
Easily toggle between light and dark themes.

```krjplmod
gui.setTheme("dark");
```

## 9. Embedding Web Content
Embed web views directly in desktop apps.

```krjplmod
let webView = gui.WebView("https://example.com");
win.add(webView);
```

## 10. Cross-Platform Deployment
Deploy applications seamlessly across Windows, Linux, and macOS.

```krjplmod
gui.build("MyApp");
```

## Conclusion
The KRJPLMod GUI Library is the ultimate toolkit for building fast, powerful, and visually appealing desktop applications. Next, explore [DOM Manipulation](dom-manipulation.md) for deeper web integration.

