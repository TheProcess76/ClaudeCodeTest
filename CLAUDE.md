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

**Commit and push after every meaningful change.** Do not batch up multiple unrelated changes into one commit. The goal is to always have GitHub reflect the current working state so work is never lost and can be reverted at any point.

```bash
git add <files>
git commit -m "short, descriptive present-tense message"
git push
```

Commit message rules:
- Use the imperative mood ("Add score reset button", not "Added" or "Adding")
- First line ≤ 72 characters; add a blank line + detail paragraph if needed
- Describe *what* changed and *why*, not *how*

Remote: https://github.com/TheProcess76/ClaudeCodeTest

## Architecture

`tictactoe.html` is structured in three sections:

- **CSS** (`<style>`): Dark-themed layout using CSS Grid for the 3×3 board, flexbox for centering. Player X uses `#e94560` (red), player O uses `#a8dadc` (teal).
- **HTML**: Static 9-cell board (`data-i` attributes 0–8), a status line, score boxes, and a reset button.
- **JavaScript** (`<script>`): Pure vanilla JS. Key globals: `board` (9-element array), `current` (active player), `gameOver`, `scores`. Win detection iterates `WINS` (8 hardcoded winning triplets). All game logic runs inside click handlers on `.cell` elements.
