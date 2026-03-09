# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-player Snake game implemented in Python using `pygame`. Single-file implementation in `snake.py`.

## Commands

- **Install dependencies:** `pip install pygame`
- **Run the game:** `python snake.py`
- **Syntax check:** `python -m py_compile snake.py`

## Architecture

- All game logic lives in `snake.py` — a standard pygame game loop pattern.
- `gameLoop()` is the main entry point containing the game state machine.
- State is managed via two boolean flags: `game_over` (exit game) and `game_close` (show loss screen).
- The game loop handles input via `pygame.event.get()`, with frame rate controlled by `clock.tick(SNAKE_SPEED)`.
- On game-over, pressing C recursively calls `gameLoop()` to restart.

## Coding Style

- Generally PEP 8, but some variables use mixed naming (e.g., `snake_List`, `Length_of_snake`).
- Colors are defined as RGB tuple constants at module level.
- Game settings (`WIDTH`, `HEIGHT`, `SNAKE_BLOCK`, `SNAKE_SPEED`) are module-level constants.

## Testing

Manual only — run the game and verify visually. No automated test suite. Use `py_compile` for syntax validation.
