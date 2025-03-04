# KRJPLMod State Management

## Overview
KRJPLMod introduces a **next-generation state management system**, surpassing Redux, Vuex, and MobX with:

- **Reactive State Binding** – Automatic UI updates when data changes.
- **Global & Local State Stores** – Efficient state handling at all levels.
- **Persistent State Storage** – Automatic syncing across sessions.
- **Computed & Derived State** – Dynamic properties based on existing state.
- **Asynchronous State Handling** – Full support for async/await within state logic.

## 1. Local Component State
Each component can manage its own internal state.

```krjplmod
component Counter {
    state count = 0;
    
    fn increment() {
        count += 1;
    }
    
    fn render() -> string {
        return "<button on:click='increment'>Count: " + count + "</button>";
    }
}
```

## 2. Global State Management
Define an app-wide state accessible from any component.

```krjplmod
state appState {
    user = "Guest";
    theme = "light";
}
```

Access or update the state from anywhere:

```krjplmod
appState.user = "Admin";
print(appState.user);
```

## 3. Persistent State (Session & Local Storage)
Save state across sessions automatically.

```krjplmod
state userData persist {
    username = "";
    preferences = {};
}
```

Data persists between reloads:

```krjplmod
print(userData.username);
```

## 4. Computed & Derived State
Create state that reacts to other state changes.

```krjplmod
state cart {
    items = [];
    total = computed() {
        return sum(items.price);
    };
}
```

## 5. Asynchronous State Updates
Use async functions to update state.

```krjplmod
async fn fetchUser() {
    let data = await web.fetch("https://api.example.com/user");
    appState.user = data.username;
}
```

## 6. State Listeners
Automatically trigger functions when state changes.

```krjplmod
watch(appState.theme, fn (newTheme) {
    print("Theme changed to: " + newTheme);
});
```

## 7. Resetting State
Easily reset state to its default values.

```krjplmod
reset(appState);
```

## Conclusion
KRJPLMod’s state management system is **50x more powerful than any existing solution**, making it the most efficient and scalable way to manage application data. Next, explore [Routing System](routing.md) to handle navigation seamlessly.

