# 👻 Haunted Library

### 🏛️ A Text-Based Adventure Game in C

**Haunted Library** is a text-based adventure game developed in C where players explore a mysterious library, solve puzzles, collect items, and uncover their way to the exit. The game combines interactive storytelling with room navigation, puzzle-solving, inventory management, and a complete user account system with multiple save slots.

Built using modular C programming, the project demonstrates concepts such as structures, file handling, modular design, string processing, and persistent game-state management.

---

## ✨ Features

### 🔐 User Authentication
- Create a new account using a username and password.
- Login using registered credentials.
- Delete accounts with password verification.
- Username and password validation.
- Account information stored locally in `users.txt`.

### 💾 Save & Load System
- Five independent save slots for every user.
- Manually save and load game progress.
- Autosave functionality through the in-game menu.
- Each save preserves the player's game state.
- Account deletion also removes associated save files.

### 🧭 Exploration & Navigation
- Navigate through different rooms using directional commands.
- Explore interconnected areas of the library.
- Inspect objects and discover hidden clues.
- Interact with objects and collect useful items.

### 🧩 Puzzle System
- Solve riddles and environment-based puzzles.
- Interact with switches and mechanisms.
- Discover clues and enter codes to progress.
- Complete the required puzzles to unlock the Exit Door.

### 🎒 Inventory Management
- Collect and manage up to 10 items.
- Use collected items to interact with the environment.
- Inventory contents persist across save and load operations.

### ❤️ Health & Game Events
- Player health system.
- Random spooky events during gameplay.
- Game progress depends on exploration and puzzle completion.

---

## 🏛️ Rooms to Explore

The game consists of eight interconnected areas, each containing unique interactions, clues, or puzzle elements.

| Room | Description |
|---|---|
| 🧪 Lab | Explore the laboratory and discover useful clues. |
| 🚪 Corridor | Navigate between different areas of the library. |
| 📦 Store Room | Search for useful items and hidden objects. |
| 🪑 Teacher's Table | Investigate objects and uncover clues. |
| 📽️ Projector Room | Interact with the projector-based puzzle. |
| 🕯️ Basement | Explore a mysterious underground area. |
| 📚 Archive | Discover information and solve challenges. |
| 🔑 Exit Door | Complete the required puzzles and find your way out. |

---

## 📁 Project Structure

The project follows a modular architecture, separating different game systems into individual source and header files.

```text
HauntedLibrary/
│
├── main.c              # Main program and game flow
│
├── auth.c              # Authentication functionality
├── auth.h
│
├── login.c             # Login and account menu
├── login.h
│
├── player.c            # Player-related functionality
├── player.h
│
├── rooms.c             # Room navigation and interactions
├── rooms.h
│
├── puzzles.c           # Puzzle logic and challenges
├── puzzles.h
│
├── save.c              # Save and load functionality
├── save.h
│
├── ui.c                # User interface and menus
├── ui.h
│
├── util.c              # Utility functions
├── util.h
│
├── Makefile            # Compilation instructions
├── README.md           # Project documentation
├── contribution.txt    # Contribution details
└── .gitignore          # Files excluded from Git
```

---

## ⚙️ Requirements & Installation

### 📌 Requirements

- GCC compiler with C11 support.
- Windows, Linux, or macOS.
- Make (optional, required only if using the Makefile).

### 📥 Clone the Repository

```bash
git clone <repository-url>
cd CProjGame
```

Replace `<repository-url>` with the URL of this GitHub repository.

### 🔨 Compilation

**Option 1: Compile directly using GCC**

Linux / macOS:

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted
```

Windows:

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted.exe
```

**Option 2: Using Make**

If Make is installed, simply execute:

```bash
make
```

The provided Makefile compiles the source files and generates the `haunted` executable.

To remove generated object files and executables:

```bash
make clean
```

To clean and rebuild:

```bash
make rebuild
```

### ▶️ Running the Game

**Linux / macOS:**

```bash
./haunted
```

**Windows (PowerShell):**

```powershell
.\haunted.exe
```

---

## 🎮 Gameplay Guide

### 🚶 Movement Commands

| Command | Description |
|---|---|
| `go north` | Move north |
| `go south` | Move south |
| `go east` | Move east |
| `go west` | Move west |

### 🔍 Interaction Commands

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

### 💾 Game Management Commands

| Command | Description |
|---|---|
| `save` | Save current progress |
| `load` | Load saved progress |
| `menu` | Open the in-game menu |
| `quit` | Exit the game |

### 📋 In-Game Menu

The in-game menu provides the following options:

1. Resume the current game.
2. Save current progress.
3. Return to the save slot menu.
4. Quit the game.

---

## 💾 Data Storage

The game uses file handling to maintain user accounts and saved game progress between sessions.

### User Database

Registered users are stored in:

```text
users.txt
```

The file follows this format:

```text
<id>:<username>:<hash>
```

### Save Files

Each user has five independent save slots.

Save files follow this naming convention:

```text
save_user_<id>_slot_<slot>.dat
```

Each save stores information such as:

- Player's current room.
- Player health.
- Inventory items.
- Puzzle states.
- Switch configurations.
- Game completion status.
- User and save slot information.

**Note:** User database and save files are generated automatically during gameplay. They are not required in the GitHub repository.

---

## ⚠️ Known Limitations

- The game currently uses a text-based interface.
- Password characters are visible during input.
- Usernames and passwords cannot contain spaces.
- Terminal appearance may vary depending on the operating system and terminal configuration.

---

## 👨‍💻 Contributors

This project was developed collaboratively.

| Contributor | Contributions |
|---|---|
| **Shubham** | Main program structure, core systems, module integration and compilation fixes. |
| **Yash** | Storyline, branching paths, in-game events and player interactions. |
| **Harsh** | Menu systems, utility functions, gameplay improvements and testing. |

For more details, refer to [contribution.txt](contribution.txt).

---

## 📜 License

This project was developed for academic and educational purposes.

---

⭐ **Enjoy exploring the Haunted Library!**