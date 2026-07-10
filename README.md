♟️ Chess Game

A fully playable chess game built with vanilla JavaScript, featuring a Human vs Human mode and a Human vs AI mode powered by the Minimax algorithm.

live demo : https://praveenkr-07.github.io/ChessGame/ 
   
Features


♜ Two Game Modes — Play against another human or challenge the built-in AI
🎨 Color Selection — Choose to play as White or Black before the game starts
🤖 AI Opponent — Computer opponent driven by the Minimax algorithm for move evaluation
✅ Full Rule Enforcement — Legal move validation, turn tracking, and standard chess rules
🔄 Replayability — "Play Again" option to reset the board and start a new game instantly
🖼️ Clean Board UI — Classic piece set with an intuitive, responsive board layout


Tech Stack


JavaScript (Vanilla) — Core game logic and board state management
HTML5 / CSS3 — Board rendering and UI layout
Minimax Algorithm — AI move selection and game-tree evaluation
Observer Pattern — Used internally to keep the board UI in sync with game state changes


How to Play


Open the live game
Select your mode: Human (vs a friend) or AI (vs the computer)
Select your color: White or Black
Click Start Game and play your moves on the board
Click Play Again anytime to reset and start a new match


Project Structure

ChessGame/
├── index.html          # Main game page
├── css/                # Styling for board and UI
├── js/                 # Game logic, move validation, AI (Minimax)
└── img/                # Chess piece assets

Getting Started Locally

bashgit clone https://github.com/praveenkr-07/ChessGame.git
cd ChessGame

Then simply open index.html in your browser — no build step or dependencies required.

Author

Praveen Kumar
GitHub: @praveenkr-07

License

This project is open source and available for learning and personal use.
