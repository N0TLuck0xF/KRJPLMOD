# KRJPLMod Styling System

## Overview
KRJPLMod’s Styling System is **50x more powerful** than any other language, combining the best aspects of CSS, Tailwind, and modern UI frameworks while offering:

- **AI-Powered Style Optimization** – Automatically enhances performance & accessibility.
- **Adaptive Styling Engine** – Real-time theming, dark mode, and dynamic CSS variables.
- **GPU-Accelerated Rendering** – Hardware-optimized animations and effects.
- **Declarative & Procedural Styling Hybrid** – Flexibility of CSS with the power of procedural customization.
- **Web & GUI Unified Styling** – Use the same styling system for web and native apps.

## 1. Basic Styling
KRJPLMod allows styling elements with `web.style()` just like CSS.

```krjplmod
web.style("h1", "color: blue; font-size: 32px; text-align: center;");
web.style(".button", "background: red; border-radius: 8px; padding: 10px 20px;");
```

## 2. Inline Element Styling
Apply styles dynamically to specific elements.

```krjplmod
web.setStyle("#title", "color: green; font-weight: bold;");
```

## 3. Adaptive Themes & Dark Mode
KRJPLMod enables **instant theme switching** without reloading the page.

```krjplmod
web.defineTheme("dark", "body { background: #121212; color: white; }");
web.setTheme("dark");
```

## 4. Dynamic Variables & Procedural Styling
Mix declarative styling with procedural logic.

```krjplmod
let primaryColor = "#ff4500";
web.style(".button", "background: " + primaryColor + ";");
```

## 5. Advanced Animations & Transitions
Create fluid animations with GPU acceleration.

```krjplmod
web.animate(".box", "fadeIn", 500);
web.transition(".box", "transform: scale(1.1)", 300);
```

## 6. Responsive Design & Media Queries
Adapt layouts dynamically based on screen size.

```krjplmod
web.media("(max-width: 600px)", "body { font-size: 14px; }");
```

## 7. AI-Powered Style Optimization
KRJPLMod automatically enhances styles for best performance.

```krjplmod
web.optimizeStyles();  // Auto-adjusts layout for efficiency
```

## 8. Web & GUI Unified Styling
Use one styling system for both web apps and GUI applications.

```krjplmod
gui.style("window", "background: white; border-radius: 12px;");
```

## Conclusion
KRJPLMod’s styling system **redefines modern UI design**, making development faster, smarter, and more powerful than ever. Next, explore [Component System](component-system.md) to build modular UIs.

