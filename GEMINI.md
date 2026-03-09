# GEMINI.md - Project Context

This document provides specialized instructional context for Gemini CLI interactions within this workspace.

## Project Overview
A simple, single-player Snake game implemented in Python using the `pygame` library. The project is designed as a lightweight, easy-to-run demonstration of 2D game mechanics, including collision detection, score tracking, and random object spawning.

**Main Technologies:**
- **Language:** Python 3.x
- **Library:** `pygame` (for graphics, event handling, and game loop management)

## Building and Running

### Prerequisites
- Python 3.x installed.
- `pygame` library installed.

### Key Commands
- **Install dependencies:**
  ```bash
  pip install pygame
  ```
- **Run the game:**
  ```bash
  python snake.py
  ```
- **Syntax Check (Verification):**
  ```bash
  python -m py_compile snake.py
  ```

## Development Conventions

### Architecture
- **Single-File Implementation:** The logic is currently contained within `snake.py` for simplicity.
- **Game Loop:** Utilizes a standard `while` loop with `pygame.event.get()` for input handling and `clock.tick(SNAKE_SPEED)` for frame rate control.
- **State Management:** Simple boolean flags (`game_over`, `game_close`) manage the transitions between playing, game-over screens, and exiting.

### Coding Style
- Follows standard Python (PEP 8) naming conventions for functions (`snake_case`) and variables, though some variable names (`snake_List`, `Length_of_snake`) reflect a more casual, beginner-friendly style.
- Uses explicit color constants defined as RGB tuples.

### Testing & Validation
- **Manual Verification:** Since it is a GUI-based game, verification is primarily done by running the game and ensuring controls and collisions behave as expected.
- **Code Integrity:** Ensure all changes maintain compatibility with the `pygame` event loop and do not introduce blocking calls that would freeze the UI.
