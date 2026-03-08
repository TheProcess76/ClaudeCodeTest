# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A browser-based Tic Tac Toe game. The entire application lives in a single self-contained HTML file (`tictactoe.html`) with inline CSS and JavaScript — no build step, no dependencies, no package manager.

## Running the project

Open `tictactoe.html` directly in a browser:

```bash
open tictactoe.html
```

## Git workflow

Every change must be committed with a clear message and pushed to GitHub:

```bash
git add <files>
git commit -m "descriptive message"
git push
```

Remote: https://github.com/TheProcess76/ClaudeCodeTest

## Architecture

`tictactoe.html` is structured in three sections:

- **CSS** (`<style>`): Dark-themed layout using CSS Grid for the 3×3 board, flexbox for centering. Player X uses `#e94560` (red), player O uses `#a8dadc` (teal).
- **HTML**: Static 9-cell board (`data-i` attributes 0–8), a status line, score boxes, and a reset button.
- **JavaScript** (`<script>`): Pure vanilla JS. Key globals: `board` (9-element array), `current` (active player), `gameOver`, `scores`. Win detection iterates `WINS` (8 hardcoded winning triplets). All game logic runs inside click handlers on `.cell` elements.
