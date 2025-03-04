# Web Development Basics in KRJPLMod

## Introduction
KRJPLMod provides a powerful, built-in web development framework that surpasses traditional languages like JavaScript, React, and Vue. This guide covers the fundamentals of building web applications with KRJPLMod.

## 1. Setting Up a Web Project
To create a new web project, run:
```bash
krjplmod new web_project --web
cd web_project
```
This sets up the necessary files and dependencies.

## 2. Creating Your First Web Page
Create `index.krjplmod` and add:
```krjplmod
web.page("Home") {
    web.h1("Welcome to KRJPLMod Web Dev!");
    web.p("Building web apps has never been easier.");
}
```
Run it:
```bash
krjplmod serve
```
Then, open `http://localhost:8000` in your browser.

## 3. Handling User Input
Add an input field and a button:
```krjplmod
web.page("User Input") {
    let name = web.input("Enter your name");
    web.button("Submit", fn() {
        web.h1("Hello, " + name);
    });
}
```
This dynamically updates the page when the button is clicked.

## 4. Working with Components
Create reusable components for modular web development:
```krjplmod
component Navbar() {
    web.nav() {
        web.link("Home", "/");
        web.link("About", "/about");
    }
}

web.page("Main") {
    Navbar();
    web.h1("KRJPLMod Web Framework");
}
```

## 5. Styling with CSS-like Syntax
KRJPLMod integrates a built-in styling system:
```krjplmod
web.style("h1", "color: blue; font-size: 24px;");
web.style("p", "font-family: Arial;");
```
This applies styles dynamically within your KRJPLMod project.

## 6. Making API Requests
Fetching data from an external API is simple:
```krjplmod
let data = web.fetch("https://api.example.com/data");
web.p("Data: " + data);
```

## Conclusion
KRJPLMod enables seamless web development with a **faster, cleaner, and more powerful syntax** than existing frameworks. Next, explore:
- [Game Development Basics](game_dev_basics.md)
- [Advanced Features](../docs/advanced_features.md)

Now, start building **next-gen web apps with KRJPLMod**!

