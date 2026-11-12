# 👻 Haunted Library

### 🏛️ A Text-Based Adventure Game in C

**Haunted Library** is a text-based adventure game developed in C where players explore a mysterious library, solve puzzles, collect items, and uncover their way to the exit.

The game combines interactive storytelling, room navigation, puzzle-solving, inventory management, and a user account system with multiple save slots. It is built using modular C programming and demonstrates concepts such as structures, file handling, string processing, and persistent game-state management.

---

## ✨ Features

### 🔐 User Account System
- Create accounts using a username and password.
- Login using registered credentials.
- Delete accounts with password verification.
- Username and password must contain at least 5 characters.
- Spaces are not allowed in usernames or passwords.
- User accounts are stored locally in `users.txt`.

### 💾 Save & Load System
- Five independent save slots for every user.
- Manually save and load game progress.
- Autosave functionality through the in-game menu.
- Each save preserves the complete player state.
- Account deletion automatically removes associated save files.

### 🧭 Exploration & Navigation
- Explore eight interconnected areas of the library.
- Move between rooms using directional commands.
- Inspect objects and discover hidden clues.
- Interact with objects and collect useful items.

### 🧩 Puzzle System
- Solve riddles and environment-based puzzles.
- Interact with switches and mechanisms.
- Discover clues and enter codes to progress.
- Complete the required puzzles to unlock the Exit Door.

### 🎒 Inventory Management
- Carry up to 10 items.
- Collect and manage items required for progression.
- Use collected items to interact with the environment.
- Inventory contents are preserved across save and load operations.

### ❤️ Health & Game Events
- Player health system.
- Random spooky events during gameplay.
- Game progression depends on exploration and puzzle completion.

---

## 🏛️ Rooms to Explore

The library consists of eight interconnected areas, each containing unique interactions, clues, or puzzle elements.

| Room | Description |
|---|---|
| 🧪 Lab | Explore the laboratory and discover useful clues. |
| 🚪 Corridor | Navigate between different areas of the library. |
| 📦 Store Room | Search for useful items and hidden objects. |
| 🪑 Teacher's Table | Investigate objects and uncover clues. |
| 📽️ Projector Room | Interact with the projector-based puzzle. |
| 🕯️ Basement | Explore the mysterious underground area. |
| 📚 Archive | Discover information and solve challenges. |
| 🔑 Exit Door | Complete the required puzzles and find your way out. |

---

## 📁 Project Structure

The project follows a modular architecture, separating different game systems into individual source and header files.

```text
Haunted-Library/
│
├── main.c              # Main program and game flow
│
├── auth.c              # Authentication functionality
├── auth.h
│
├── login.c             # Login and account management
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
- Make (optional, required only when using the Makefile).

### 📥 Clone the Repository

Open your terminal and execute:

```bash
git clone https://github.com/harsh-1507/Haunted-Library.git
```

Navigate to the project directory:

```bash
cd Haunted-Library
```

### 🔨 Compilation

**Option 1: Using Make (Recommended)**

If Make is installed, simply execute:

```bash
make
```

The provided Makefile automatically compiles the source files and generates the `haunted` executable.

**Option 2: Using GCC Directly**

If Make is unavailable, compile all source files directly.

Linux / macOS:

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted
```

Windows (MinGW GCC):

```bash
gcc -std=c11 -O2 -Wall -Wextra main.c login.c auth.c player.c rooms.c puzzles.c save.c util.c ui.c -o haunted.exe
```

### 🧹 Cleaning Generated Files

To remove generated object files and executables:

```bash
make clean
```

To clean and rebuild the project:

```bash
make rebuild
```

---

## ▶️ Running the Game

Once compilation is successful, run the executable.

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

### 👤 User Database

Registered users are stored in:

```text
users.txt
```

The file follows this format:

```text
<id>:<username>:<hash>
```

### 💾 Save Files

Each registered user has five independent save slots.

Save files follow this naming convention:

```text
save_user_<id>_slot_<slot>.dat
```

Each save stores information such as:

- Current room.
- Player health.
- Inventory items.
- Puzzle states.
- Switch configurations.
- Game completion status.
- User ID and save slot information.

**Note:** User database and save files are generated automatically during gameplay and are not included in the GitHub repository.

---

## ⚠️ Known Limitations

- The game currently uses a text-based interface.
- Password characters are visible while typing.
- Spaces are not allowed in usernames or passwords.
- Terminal appearance may vary depending on the operating system.
- Colored terminal output on Windows depends on ANSI terminal support.

---

## 👨‍💻 Contributors

This project was developed collaboratively by:

| Contributor | Contributions |
|---|---|
| **Shubham** | Main program structure, core systems, module integration, header organization and compilation fixes. |
| **Yash** | Storyline, branching paths, in-game events, input/output and interaction-based functions. |
| **Harsh** | Menu systems, utility functions, gameplay improvements, logic refinement and testing. |

For more details, refer to [contribution.txt](contribution.txt).

---

## 📜 License

This project was developed for academic and educational purposes.

---

⭐ **Enjoy exploring the Haunted Library!**