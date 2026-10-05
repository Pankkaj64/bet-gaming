# Bet Gaming: Console Slot Machine

A command-line slot machine game written in Node.js. You deposit a starting balance, choose how many lines to bet on, place a bet per line, and spin a 3x3 reel. Matching rows pay out based on the symbol's value, and you can keep playing until you stop or run out of money.

## Features

- Interactive terminal prompts for the deposit, number of lines (1-3) and bet per line
- Input validation that re-prompts on invalid numbers, non-whole or out-of-range line counts, or bets larger than the balance allows
- 3x3 slot machine spin using weighted symbols (`A` is rarest, `D` most common), drawn without replacement on each reel
- Reels are transposed into rows and printed as `A | B | C`
- Payouts for every bet line where all three symbols match, multiplied by the symbol's value (`A` x5, `B` x4, `C` x3, `D` x2)
- Running balance that updates after every spin, with a play-again loop and a game-over message when the balance hits zero

## Tech Stack

- JavaScript (Node.js, CommonJS)
- [prompt-sync](https://www.npmjs.com/package/prompt-sync) for synchronous terminal input

## Project Structure

```
bet-gaming/
├── project.js         # Game logic: deposit, bet, spin, payout and game loop
├── package.json       # Project metadata, start script and the prompt-sync dependency
├── package-lock.json  # Locked dependency versions
└── .gitignore         # Keeps node_modules out of version control
```

## Getting Started

Requires [Node.js](https://nodejs.org/).

```bash
git clone https://github.com/Pankkaj64/bet-gaming.git
cd bet-gaming
npm install
npm start
```

Follow the prompts in the terminal to deposit, bet and spin. Answer `y` to spin again, anything else to cash out, or press `Ctrl+C` to quit at any time.

## Example

```
Enter a deposit amount: 100
You have a balance of $100
Enter the number of lines to bet on (1-3): 2
Enter the bet per line: 10
A | D | A
C | B | C
C | D | D
You won, $0
Do you want to play again (y/n)? n
```
