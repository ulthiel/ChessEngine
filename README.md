# ChessEngine
Python 3 UCI chess engine

## Introduction
There are three main subtasks in this repository:
1. Board evaluation
2. Move generation using search algorithms (pruning and other heuristic analysis)
3. Opening database

This is a Universal Chess Interface engine and uses the [lichess-bot bridge](https://github.com/careless25/lichess-bot) to play on lichess.org.

## Requirements:
1. [python-chess](https://github.com/niklasf/python-chess) for board representation
2. [lichess-bot](https://github.com/careless25/lichess-bot) if you want it to play as a bot on lichess

## Fixes by UT
1. Fixed the negamax and the search function (engine was maxizing damage before...).
2. Fixed parsing of ```position startpos``` command. E.g. the following command sequence did not work (but is sent for example when using an opening book for the first few moves):
```
uci
ucinewgame
position startpos
position startpos moves g2g4 e7e5
```
3. Added functionality for ```position fen``` command.
