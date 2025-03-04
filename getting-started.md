# Getting Started with KRJPLMod

## Introduction
Welcome to KRJPLMod! This guide will walk you through setting up your development environment and writing your first program.

## 1. Installing KRJPLMod
KRJPLMod can be installed via package managers or manually:

### Installation via Package Manager
```bash
krjplmod install
```

### Manual Installation
1. Download the latest release from the official repository.
2. Extract the files.
3. Run the setup script:
```bash
./setup.sh
```

## 2. Setting Up a Project
Create a new KRJPLMod project with:
```bash
krjplmod new my_project
cd my_project
```

## 3. Writing Your First Program
Create a new file `main.krjplmod` and add:
```krjplmod
fn main() {
    print("Hello, KRJPLMod!");
}
```
Run it with:
```bash
krjplmod run main.krjplmod
```

## 4. Using the KRJPLMod REPL
Launch an interactive shell:
```bash
krjplmod repl
```
Test simple commands:
```krjplmod
print("Live coding in KRJPLMod!");
```

## 5. Understanding the Project Structure
A typical KRJPLMod project includes:
```
/my_project
 ├── main.krjplmod  # Entry point
 ├── modules/       # Additional scripts
 ├── assets/        # Static files
 ├── config.json    # Project settings
```

## 6. Next Steps
Now that you’re set up, explore:
- [Web Development Basics](web_dev_basics.md)
- [Game Development Basics](game_dev_basics.md)

Happy coding with KRJPLMod!

