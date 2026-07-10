# Chess Game

A fully playable, lightweight Chess implementation built with vanilla JavaScript, HTML5, and CSS3. The project provides both Human vs Human and Human vs AI gameplay — the AI is implemented using a Minimax search with a simple evaluation function. This repository is intended for learning, experimentation, and small-scale demonstrations.

Live demo: https://praveenkr-07.github.io/ChessGame/

## Highlights

- Two game modes: Human vs Human and Human vs AI
- Clean, responsive UI with classic piece set
- AI opponent driven by a Minimax algorithm with a configurable search depth
- Full rule enforcement: legal-move validation, turn tracking, captures, promotion, castling, check and checkmate detection
- No build step or external dependencies — open `index.html` in a browser to play

## Edge cases handled (10)

This implementation explicitly addresses the following edge cases and special rules of chess:

1. Pawn promotion: pawns that reach the last rank are promoted to a queen and the promotion event is emitted.
2. Castling (both king- and queen-side): castling is allowed only when the king and the appropriate rook have not moved, the path is clear, and none of the squares the king traverses are under attack.
3. Pawn double-step on first move: pawns can move two squares from their initial rank when unobstructed.
4. Pawn captures vs forward movement: pawn attack moves (diagonals) are handled separately from straight advances and blocked correctly.
5. Move filtering to stay on-board: generated moves that would fall outside the 8x8 board are discarded.
6. Prevention of moves that leave the king in check: candidate moves are validated to ensure the player's own king is not left in check after the move.
7. Check detection: identifies when a player's king is under attack and emits a 'check' event.
8. Checkmate detection: determines when the player has no legal moves and is in check, emitting a 'checkMate' event.
9. Capture and undo semantics: captures remove pieces from active lists and undo restores piece positions and captured pieces as needed (including reversal of castling state).
10. Robust piece movement rules: per-piece movement patterns (rook, bishop, queen, knight, king, pawn) are enforced with ray-tracing and blocking logic so sliding pieces stop at obstructions and knights use fixed offsets.

These cover the core special rules and many common edge cases required for correct gameplay. Note: this project focuses on practical gameplay and a straightforward Minimax AI; advanced tournament rules such as insufficient material draws, threefold repetition, and the fifty-move rule are not implemented.

## Tech stack

- JavaScript (vanilla) — game logic, move validation, AI (Minimax)
- HTML5 / CSS3 — UI and board rendering

## Project structure

ChessGame/
├── index.html          # Main game page
├── chess.css           # Styling for board and UI
├── Board.js            # Board rendering / UI helpers
├── Game.js             # Core game state, rules enforcement, events, and history
├── History.js          # Move history / undo support
├── SimulationGame.js   # Lightweight game instance used by the AI for lookahead
├── ai.js               # Minimax-based AI
├── piece.js            # Per-piece movement generators and utilities
└── img/                # Chess piece assets

## How to play

1. Open the live demo or open `index.html` locally in your browser.
2. Select the desired mode: Human (play a friend) or AI (play against the computer).
3. Choose a color (White or Black) and start the game.
4. Use the "Play Again" button to reset the board and start a new match.

## Running locally

```bash
git clone https://github.com/praveenkr-07/ChessGame.git
cd ChessGame
# Open index.html in your browser (no build step required)
```

## Author

Praveen Kumar — GitHub: @praveenkr-07

## License

This project is open source and provided for educational and personal use.
