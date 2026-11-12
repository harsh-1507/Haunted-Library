# 👻 Haunted Library

A **text-based adventure game developed in C** where players explore a mysterious library, solve puzzles, collect items, and uncover their way to the exit. The game features user authentication, room navigation, inventory management, and multiple save slots for an interactive gaming experience.

## ✨ Features

- 🔐 **User Authentication:** Create accounts, log in, and delete accounts with password verification.
- 💾 **Multiple Save Slots:** Each user gets five independent save slots.
- 🚪 **Room Navigation:** Explore different rooms using directional commands.
- 🧩 **Puzzle System:** Solve riddles, interact with objects, and complete environment-based puzzles.
- 🎒 **Inventory Management:** Collect and manage items required for progression.
- ❤️ **Health System:** Maintain player health while encountering random spooky events.
- 🔄 **Save & Load:** Save game progress manually or through autosave functionality.
- 🎮 **Interactive Menus:** Navigate through account, save slot, and in-game menus.
- 🛠️ **Modular Architecture:** Organized implementation using separate C source and header files.

## 📁 Project Structure

```text
HauntedLibrary/
│
├── main.c
├── auth.c
├── auth.h
├── login.c
├── login.h
├── player.c
├── player.h
├── rooms.c
├── rooms.h
├── puzzles.c
├── puzzles.h
├── save.c
├── save.h
├── ui.c
├── ui.h
├── util.c
├── util.h
│
├── Makefile
├── README.md
├── contribution.txt
└── .gitignore
```

## ⚙️ Requirements & Installation

### 📌 Requirements

- GCC compiler (supporting C11)
- Git (optional, for cloning the repository)
- Make (optional, for using the Makefile)

### 📥 Clone the Repository

```bash
git clone <repository-url>
cd HauntedLibrary
```

### 🔨 Compile the Project

**Option 1: Using GCC directly**

Linux / macOS:

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted
```

Windows:

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted.exe
```

**Option 2: Using Make**

```bash
make
```

The Makefile automatically compiles the source files and generates the executable.

## ▶️ Running the Game

**Linux / macOS:**

```bash
./haunted
```

**Windows:**

```powershell
.\haunted.exe
```

## 🎮 Gameplay Commands

### 🚶 Movement

| Command | Description |
|---|---|
| `go north` | Move north |
| `go south` | Move south |
| `go east` | Move east |
| `go west` | Move west |

### 🔍 Interaction

| Command | Description |
|---|---|
| `look` | View the current room |
| `take <item>` | Pick up an item |
| `inspect <object>` | Inspect an object |
| `read riddle` | Read a riddle |
| `solve projector` | Interact with the projector puzzle |
| `flip 1/2/3` | Operate puzzle switches |
| `enter code ####` | Enter a puzzle code |
| `use student id` | Use the student ID |
| `inventory` or `i` | View collected items |
| `help` | Display available commands |

### 💾 Game Management

| Command | Description |
|---|---|
| `save` | Save current progress |
| `load` | Load saved progress |
| `menu` | Open the in-game menu |
| `quit` | Exit the game |

## 💾 Game Progress & Data Storage

The game maintains user accounts and individual save files.

- `users.txt` stores registered user information.
- Each account has five save slots.
- Save files store the player's game state, including room position, health, inventory, and puzzle progress.
- Account deletion removes the associated save files.

These files are generated automatically when the game is used and do not need to be included in the repository.

## 👨‍💻 Contributors

- **Shubham** – Core program structure, module integration, and major game systems.
- **Yash** – Storyline, branching paths, game events, and player interactions.
- **Harsh** – Menu systems, utility functions, gameplay improvements, and testing.

See [contribution.txt](contribution.txt) for more details about individual contributions.

## 📜 License

This project was developed for academic and educational purposes.

---

⭐ If you find this project interesting, consider giving it a star!