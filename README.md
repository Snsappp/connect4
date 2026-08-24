# Connect4 AI

My first real front-end project. It's a browser-based Connect 4 game where you play against an AI opponent. No frameworks, no build tools   just HTML, CSS, and vanilla JavaScript in one file.

![status](https://img.shields.io/badge/status-working-brightgreen)

## What it does

- Play Connect 4 against a computer opponent
- Switch between two board sizes (7x4 or 7x5)
- Choose whether you or the AI goes first
- Pieces animate when they drop into the grid

## Why the AI is actually decent

I didn't want to just make a bot that plays randomly or only looks one move ahead. The AI uses **minimax with alpha-beta pruning**, which basically means it looks several moves into the future and tries to pick the move that leads to the best outcome, while also cutting off branches it doesn't need to fully explore (that's the "pruning" part   it saves a ton of computation).

On top of that it:
- Takes an instant win if one is available
- Blocks you if you're one move from winning
- Checks a few moves ahead for "forced win" traps so it doesn't accidentally set you up to win
- Weighs center column control a bit higher, since center pieces tend to be more useful in Connect 4

It's not unbeatable, but it plays legit   you have to actually think.

## How to run it

There's no build step. Just open `index.html` in your browser and start playing. That's it.

## How to play

1. Pick a board size at the top
2. Pick who goes first
3. Click a column to drop your piece
4. Get four in a row (horizontal, vertical, or diagonal) before the AI does

## What I learned building this

- How minimax and alpha-beta pruning actually work once you implement them instead of just reading about them
- Manipulating a grid with vanilla JS and keeping the DOM in sync with a game state array
- CSS animations for something as simple as a piece "dropping" into place
- Recursion is a lot easier to reason about when you're the one debugging it at 1am

## Things I'd like to add eventually

- A way to undo a move
- Difficulty levels (right now it's basically always playing near-optimally)
- Better mobile layout
- Maybe a win-streak counter or some kind of score tracking

## Notes

This was built as a learning project, so the code isn't perfectly clean everywhere   it's a work in progress like I am. Feedback welcome if you spot something dumb.

snsappp.github.io/connect4/
