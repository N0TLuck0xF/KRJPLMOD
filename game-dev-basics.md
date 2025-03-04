# Game Development Basics in KRJPLMod

## Introduction
KRJPLMod provides a built-in game development framework that is more efficient and feature-rich than existing engines like Unity and Unreal Engine. This guide covers the basics of creating interactive 2D and 3D games using KRJPLMod.

## 1. Setting Up a Game Project
To start a new game project, run:
```bash
krjplmod new game_project --game
cd game_project
```
This sets up the necessary files and engine configurations.

## 2. Creating a Game Window
Define a simple game window:
```krjplmod
game.window("My First Game", 800, 600);
```
This opens a game window with a width of 800 and a height of 600 pixels.

## 3. Adding a Player Object
Define a player character using the built-in sprite system:
```krjplmod
let player = game.sprite("player.png", 100, 100);
game.add(player);
```
This loads the player sprite and places it at coordinates (100, 100).

## 4. Handling Player Input
Move the player using keyboard input:
```krjplmod
game.on_key("ArrowRight", fn() {
    player.move(10, 0);
});

game.on_key("ArrowLeft", fn() {
    player.move(-10, 0);
});
```

## 5. Adding Physics and Collisions
Enable physics for the player and detect collisions:
```krjplmod
player.enable_physics();
player.on_collision("enemy", fn() {
    game.over("You lost!");
});
```

## 6. Rendering the Game Loop
Define the main game loop:
```krjplmod
game.loop(fn() {
    player.update();
    game.render();
});
```

## 7. Creating Enemy AI
Add a basic enemy with movement logic:
```krjplmod
let enemy = game.sprite("enemy.png", 500, 100);

game.loop(fn() {
    enemy.move_towards(player, 2);
});
```

## 8. Adding Sound Effects
Play sound effects on events:
```krjplmod
game.sound("jump.wav").play();
```

## 9. Exporting the Game
To build and export your game, run:
```bash
krjplmod build --game
```
This compiles your game into an executable format.

## Conclusion
KRJPLMod makes game development **faster, easier, and more powerful** than any existing engine. Now, explore:
- [Advanced Features](../docs/advanced_features.md)
- [AI Integration](../use_cases/ai_integration.md)

Start building **next-gen games with KRJPLMod**!

