# Connect Four AI player

For CS 111, Introduction to Computer Science, with Erik Carlson

We made a connect 4 game which utilizes python's built in turtle objects to draw
the board and various pieces on the board. Additionally, we created an ai which
utilizes a mini-max algorithm optimized with alpha beta pruning to find the
best possible move based on a scoring system that evaluates a given new piece.

See [project requirements](Requirements.pdf)

<p align="center">
<img src="./AI_player.gif" alt="AI playing" width="500" />
</p>
<p align="center">
AI playing yellow pieces exploring 5 moves in advance
</p>

## To Run
Double click on our run.py, or run in the terminal directory

```
python3 run.py
```

## Classes
We made classes for each type of object that we use in our code. This includes
a class for the board, graphics, ai, playon (a class which controls
various aspects of the game) and run (a class which connect all the other
classes together). We made these classes to easily access data in
the whole program, and we made sure that our classes cover a more general case.
These will enable us to make variations on things to use in other classes
(e.g. created a new board in the ai class to test various moves on).

## Testing
We have two files that are not used within the program: check_winning_algorithm.py and
check_ai_algorithm.py. While not utilized in the program itself, these files were used
to test our endgame function and test that our ai evaluates the correct
score in certain situations.

## Suggestions
For graphics, we could have made the game a little more flashy, or added
additional features, but all of the necessities are there. When initialized, the
board gives the user 3 options: (human vs. human, human vs. ai, and ai vs. ai).
While the 'ai vs. ai' option was mostly designed for testing our ai and
checking for bugs, it is still interesting to see the computer play against
itself. After the user has made their choice, our program displays all the
pieces and the board. The user can click the desired spot to place a piece. They
must click the actual space and not above or where another piece already is. If
a player clicks an invalid spot a message will be put in the terminal, and the
program will wait for a valid move. 

## Issues
Currently, our program does not have any known bugs, and the only issue that
can occur is long waiting times when the ai is set to search more than 5 moves
in advance. Therefore we will set the depth of the mini-max algorithm fairly
low to 5 maintain a reasonable computation time.

## Usage

```
usage: run.py [-h] [--ai-type MINIMAX or RANDOM]
              [--ai-strength RECURSIVE DEPTH]

Connect4 AI

optional arguments:
  -h, --help            show this help message and exit
  --ai-type MINIMAX or RANDOM
                        smart (minimax) or random AI algorithm (default:
                        smart)
  --ai-strength RECURSIVE DEPTH
                        (--ai-type=minimax only) algorithm search depth
                        (default: 5)
```